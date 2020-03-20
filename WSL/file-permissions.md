---
title: Autorisations de fichiers
description: Comprendre comment WSL détermine les autorisations de fichiers dans Windows
keywords: BashOnWindows, bash, WSL, wsl2, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, Debian, SUSE, Windows 10, fichier, autorisations
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4566fc86cf14df986bde80cf3a6cfb9267b23308
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520858"
---
# <a name="file-permissions-for-wsl"></a><span data-ttu-id="984b9-104">Autorisations de fichier pour WSL</span><span class="sxs-lookup"><span data-stu-id="984b9-104">File Permissions for WSL</span></span>

<span data-ttu-id="984b9-105">Cette page explique en détail comment les autorisations des fichiers Linux sont interprétées dans le sous-système Windows pour Linux, en particulier lors de l’accès à des ressources dans Windows sur le système de fichiers NT.</span><span class="sxs-lookup"><span data-stu-id="984b9-105">This page details how Linux file permissions are interpreted across the Windows Subsystem for Linux, especially when accessing resources inside of Windows on the NT file system.</span></span> <span data-ttu-id="984b9-106">Cette documentation suppose une connaissance élémentaire de la [structure des autorisations du système de fichiers Linux](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="984b9-106">This documentation assumes a basic understanding of the [Linux file system permissions structure](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)</span></span> <!--TODO: Double check that it's okay to add these links--> <span data-ttu-id="984b9-107">et la [commande umask](https://en.wikipedia.org/wiki/Umask).</span><span class="sxs-lookup"><span data-stu-id="984b9-107">and the [umask command](https://en.wikipedia.org/wiki/Umask).</span></span>

<span data-ttu-id="984b9-108">Lors de l’accès aux fichiers Windows à partir de WSL, les autorisations de fichiers sont calculées à partir des autorisations Windows ou lues à partir de métadonnées qui ont été ajoutées au fichier par WSL.</span><span class="sxs-lookup"><span data-stu-id="984b9-108">When accessing Windows files from WSL the file permissions are either calculated from Windows permissions, or are read from metadata that has been added to the file by WSL.</span></span> <span data-ttu-id="984b9-109">Ces métadonnées ne sont pas activées par défaut.</span><span class="sxs-lookup"><span data-stu-id="984b9-109">This metadata is not enabled by default.</span></span> 

## <a name="wsl-metadata-on-windows-files"></a><span data-ttu-id="984b9-110">WSL les métadonnées sur les fichiers Windows</span><span class="sxs-lookup"><span data-stu-id="984b9-110">WSL metadata on Windows files</span></span>

<span data-ttu-id="984b9-111">Lorsque les métadonnées sont activées en tant qu’option de montage dans WSL, les attributs étendus des fichiers Windows NT peuvent être ajoutés et interprétés pour fournir des autorisations de système de fichiers Linux.</span><span class="sxs-lookup"><span data-stu-id="984b9-111">When metadata is enabled as a mount option in WSL, extended attributes on Windows NT files can be added and interpreted to supply Linux file system permissions.</span></span> 

<span data-ttu-id="984b9-112">WSL peut ajouter quatre attributs étendus NTFS :</span><span class="sxs-lookup"><span data-stu-id="984b9-112">WSL can add four NTFS extended attributes:</span></span>

| <span data-ttu-id="984b9-113">Nom de l’attribut</span><span class="sxs-lookup"><span data-stu-id="984b9-113">Attribute Name</span></span> | <span data-ttu-id="984b9-114">Description</span><span class="sxs-lookup"><span data-stu-id="984b9-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="984b9-115">$LXUID</span><span class="sxs-lookup"><span data-stu-id="984b9-115">$LXUID</span></span> | <span data-ttu-id="984b9-116">ID du propriétaire de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="984b9-116">User Owner ID</span></span> |
| <span data-ttu-id="984b9-117">$LXGID</span><span class="sxs-lookup"><span data-stu-id="984b9-117">$LXGID</span></span> | <span data-ttu-id="984b9-118">ID du propriétaire du groupe</span><span class="sxs-lookup"><span data-stu-id="984b9-118">Group Owner ID</span></span> |
| <span data-ttu-id="984b9-119">$LXMOD</span><span class="sxs-lookup"><span data-stu-id="984b9-119">$LXMOD</span></span> | <span data-ttu-id="984b9-120">Mode de fichier (autorisations des systèmes de fichiers octaux et type, par exemple : 0777)</span><span class="sxs-lookup"><span data-stu-id="984b9-120">File mode (File systems permission octals and type, e.g: 0777)</span></span> |
| <span data-ttu-id="984b9-121">$LXDEV</span><span class="sxs-lookup"><span data-stu-id="984b9-121">$LXDEV</span></span> | <span data-ttu-id="984b9-122">Appareil, s’il s’agit d’un fichier d’appareil</span><span class="sxs-lookup"><span data-stu-id="984b9-122">Device, if it is a device file</span></span> |

<span data-ttu-id="984b9-123">En outre, tout fichier qui n’est pas un fichier ou un répertoire normal (par exemple, liens symboliques, FIFO, Block Devices, les sockets Unix et les périphériques de caractères) a également un [point d’analyse](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)NTFS.</span><span class="sxs-lookup"><span data-stu-id="984b9-123">Additionally, any file that is not a regular file or directory (e.g: symlinks, FIFOs, block devices, unix sockets, and character devices) also have an NTFS [reparse point](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points).</span></span> <span data-ttu-id="984b9-124">Il est ainsi beaucoup plus rapide de déterminer le type de fichier dans un répertoire donné sans avoir à interroger ses attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="984b9-124">This makes it much faster to determine the kind of file in a given directory without having to query its extended attributes.</span></span> 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a><span data-ttu-id="984b9-125">Scénarios d’accès aux fichiers</span><span class="sxs-lookup"><span data-stu-id="984b9-125">File Access Scenarios</span></span>

<span data-ttu-id="984b9-126">Vous trouverez ci-dessous une description de la façon dont les autorisations sont déterminées lors de l’accès aux fichiers de différentes manières à l’aide du sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="984b9-126">Below is a description of how permissions are determined when accessing files in different ways using the Windows Subsystem for Linux.</span></span>

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a><span data-ttu-id="984b9-127">Accès aux fichiers dans le système de fichiers du lecteur Windows (DrvFS) à partir de Linux</span><span class="sxs-lookup"><span data-stu-id="984b9-127">Accessing Files in the Windows drive file system (DrvFS) from Linux</span></span>

<span data-ttu-id="984b9-128">Ces scénarios se produisent lorsque vous accédez à vos fichiers Windows à partir de WSL, très probablement via `/mnt/c`.</span><span class="sxs-lookup"><span data-stu-id="984b9-128">These scenarios occur when you are accessing your Windows files from WSL, most likely via `/mnt/c`.</span></span> 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a><span data-ttu-id="984b9-129">Lecture des autorisations de fichier à partir d’un fichier Windows existant</span><span class="sxs-lookup"><span data-stu-id="984b9-129">Reading file permissions from an existing Windows file</span></span>

<span data-ttu-id="984b9-130">Le résultat dépend de si le fichier a déjà des métadonnées existantes.</span><span class="sxs-lookup"><span data-stu-id="984b9-130">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="984b9-131">**Le fichier ne contient pas de métadonnées (par défaut)**</span><span class="sxs-lookup"><span data-stu-id="984b9-131">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="984b9-132">Si le fichier n’a pas de métadonnées qui lui sont associées, nous traduisons les autorisations effectives de l’utilisateur Windows en lecture/écriture/exécution des bits et leur attribuons la même valeur pour l’utilisateur, le groupe et l’autre.</span><span class="sxs-lookup"><span data-stu-id="984b9-132">If the file has no metadata associated with it then we translate the effective permissions of the Windows user to read/write/execute bits and set them to the this as the same value for user, group, and other.</span></span> <span data-ttu-id="984b9-133">Par exemple, si votre compte d’utilisateur Windows dispose d’un accès en lecture et en écriture, mais pas d’un accès en écriture au fichier, ce sera affiché comme `r-x` pour utilisateur, groupe et autre.</span><span class="sxs-lookup"><span data-stu-id="984b9-133">For example, if your Windows user account has read and execute access but not write access to the file then this will be shown as `r-x` for user, group and other.</span></span> <span data-ttu-id="984b9-134">Si l’attribut « lecture seule » du fichier est défini dans Windows, nous n’accordons pas d’accès en écriture dans Linux.</span><span class="sxs-lookup"><span data-stu-id="984b9-134">If the file has the 'Read Only' attribute set in Windows then we do not grant write access in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="984b9-135">Le fichier contient des métadonnées</span><span class="sxs-lookup"><span data-stu-id="984b9-135">The file has metadata</span></span>

<span data-ttu-id="984b9-136">Si le fichier contient des métadonnées, nous utilisons simplement ces valeurs de métadonnées au lieu de traduire les autorisations effectives de l’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="984b9-136">If the file has metadata present, we simply use those metadata values instead of translating effective permissions of the Windows user.</span></span>

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a><span data-ttu-id="984b9-137">Modification des autorisations de fichier sur un fichier Windows existant à l’aide de chmod</span><span class="sxs-lookup"><span data-stu-id="984b9-137">Changing file permissions on an existing Windows file using chmod</span></span>

<span data-ttu-id="984b9-138">Le résultat dépend de si le fichier a déjà des métadonnées existantes.</span><span class="sxs-lookup"><span data-stu-id="984b9-138">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="984b9-139">**Le fichier ne contient pas de métadonnées (par défaut)**</span><span class="sxs-lookup"><span data-stu-id="984b9-139">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="984b9-140">Chmod n’aura qu’un seul effet. Si vous supprimez tous les attributs d’écriture d’un fichier, l’attribut « lecture seule » du fichier Windows est défini, car il s’agit du même comportement que CIFS (Common Internet File System) qui est le client SMB (Server Message Block) dans Linux.</span><span class="sxs-lookup"><span data-stu-id="984b9-140">Chmod will only have one effect, if you remove all the write attributes of a file then the 'read only' attribute on the Windows file will be set, since this is the same behaviour as CIFS (Common Internet File System) which is the SMB (Server Message Block) client in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="984b9-141">Le fichier contient des métadonnées</span><span class="sxs-lookup"><span data-stu-id="984b9-141">The file has metadata</span></span>

<span data-ttu-id="984b9-142">Chmod change ou ajoute des métadonnées en fonction des métadonnées existantes du fichier.</span><span class="sxs-lookup"><span data-stu-id="984b9-142">Chmod will change or add metadata depending on the file's already existing metadata.</span></span> 

<span data-ttu-id="984b9-143">N’oubliez pas que vous ne pouvez pas vous accorder plus d’accès que ce que vous avez sur Windows, même si les métadonnées indiquent que c’est le cas.</span><span class="sxs-lookup"><span data-stu-id="984b9-143">Please keep in mind that you cannot give yourself more access than what you have on Windows, even if the metadata says that is the case.</span></span> <span data-ttu-id="984b9-144">Par exemple, vous pouvez définir les métadonnées pour qu’elles s’affichent pour que vous disposiez d’autorisations d’accès en écriture à un fichier à l’aide de `chmod 777`, mais si vous tentez d’accéder à ce fichier, vous ne pourrez toujours pas écrire dessus.</span><span class="sxs-lookup"><span data-stu-id="984b9-144">For example, you could set the metadata to display that you have write permissions to a file using `chmod 777`, but if you tried to access that file you would still not be able to write to it.</span></span> <span data-ttu-id="984b9-145">Grâce à l’interopérabilité, les commandes de lecture ou d’écriture des fichiers Windows sont routées via vos autorisations d’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="984b9-145">This is thanks to interopability, as any read or write commands to Windows files are routed through your Windows user permissions.</span></span>

#### <a name="creating-a-file-in-drivefs"></a><span data-ttu-id="984b9-146">Création d’un fichier dans DriveFS</span><span class="sxs-lookup"><span data-stu-id="984b9-146">Creating a file in DriveFS</span></span>

<span data-ttu-id="984b9-147">Le résultat dépend de si les métadonnées sont activées.</span><span class="sxs-lookup"><span data-stu-id="984b9-147">The result depends on if metadata is enabled.</span></span>

##### <a name="metadata-is-not-enabled-default"></a><span data-ttu-id="984b9-148">Les métadonnées ne sont pas activées (par défaut)</span><span class="sxs-lookup"><span data-stu-id="984b9-148">Metadata is not enabled (default)</span></span>

<span data-ttu-id="984b9-149">Les autorisations Windows du fichier nouvellement créé sont les mêmes que si vous avez créé le fichier dans Windows sans un descripteur de sécurité spécifique, il hérite des autorisations du parent.</span><span class="sxs-lookup"><span data-stu-id="984b9-149">The Windows permissions of the newly created file will be the same as if you created the file in Windows without a specific security descriptor, it will inherit the parent's permissions.</span></span> 

##### <a name="metadata-is-enabled"></a><span data-ttu-id="984b9-150">Les métadonnées sont activées</span><span class="sxs-lookup"><span data-stu-id="984b9-150">Metadata is enabled</span></span>

<span data-ttu-id="984b9-151">Les bits d’autorisation du fichier sont définis de façon à suivre l’umask Linux, et le fichier est enregistré avec les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="984b9-151">The file's permission bits are set to follow the Linux umask, and the file will be saved with metadata.</span></span>

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a><span data-ttu-id="984b9-152">Quel utilisateur Linux et quel groupe Linux possède le fichier ?</span><span class="sxs-lookup"><span data-stu-id="984b9-152">Which Linux user and Linux group owns the file?</span></span> 

<span data-ttu-id="984b9-153">Le résultat dépend de si le fichier a déjà des métadonnées existantes.</span><span class="sxs-lookup"><span data-stu-id="984b9-153">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="984b9-154">**Le fichier ne contient pas de métadonnées (par défaut)**</span><span class="sxs-lookup"><span data-stu-id="984b9-154">**The file does not have metadata (default)**</span></span>
<span data-ttu-id="984b9-155">Dans le scénario par défaut, lors du montage automatique de lecteurs Windows, nous spécifions que l’ID d’utilisateur (UID) de tous les fichiers est défini sur l’ID d’utilisateur de votre utilisateur WSL et que l’ID de groupe (GID) est défini sur l’ID de groupe principal de votre utilisateur WSL.</span><span class="sxs-lookup"><span data-stu-id="984b9-155">In the default scenario, when automounting Windows drives, we specify that the user ID (UID) for any file is set to the user ID of your WSL user and the group ID (GID) is set to the principal group ID of your WSL user.</span></span> 

##### <a name="the-file-has-metadata"></a><span data-ttu-id="984b9-156">Le fichier contient des métadonnées</span><span class="sxs-lookup"><span data-stu-id="984b9-156">The file has metadata</span></span>

<span data-ttu-id="984b9-157">L’UID et le GID spécifiés dans les métadonnées sont appliqués en tant que propriétaire de l’utilisateur et propriétaire du fichier.</span><span class="sxs-lookup"><span data-stu-id="984b9-157">The UID and GID specified in the metadata is applied as the user owner and group owner of the file.</span></span> 

### <a name="accessing-linux-files-from-windows-using-wsl"></a><span data-ttu-id="984b9-158">Accès aux fichiers Linux à partir de Windows à l’aide de `\\wsl$`</span><span class="sxs-lookup"><span data-stu-id="984b9-158">Accessing Linux files from Windows using `\\wsl$`</span></span>

<span data-ttu-id="984b9-159">L’accès aux fichiers Linux via `\\wsl$` utilise l’utilisateur par défaut de votre distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="984b9-159">Accessing Linux files via `\\wsl$` will use the default user of your WSL distro.</span></span> <span data-ttu-id="984b9-160">Par conséquent, toute application Windows accédant à des fichiers Linux aura les mêmes autorisations que l’utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="984b9-160">Therefore any Windows app accessing Linux files will have the same permissions as the default user.</span></span>

#### <a name="creating-a-new-file"></a><span data-ttu-id="984b9-161">Création d’un nouveau fichier</span><span class="sxs-lookup"><span data-stu-id="984b9-161">Creating a new file</span></span>

<span data-ttu-id="984b9-162">L’umask par défaut est appliqué lors de la création d’un nouveau fichier à l’intérieur d’un WSL distribution à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="984b9-162">The default umask is applied when creating a new file inside of a WSL distro from Windows.</span></span> <span data-ttu-id="984b9-163">L’umask par défaut est `022`, ou en d’autres termes, il autorise toutes les autorisations, à l’exception des autorisations d’écriture sur les groupes et autres.</span><span class="sxs-lookup"><span data-stu-id="984b9-163">The default umask is `022`, or in other words it allows all permissions except write permissions to groups and others.</span></span> 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a><span data-ttu-id="984b9-164">Accès aux fichiers dans le système de fichiers racine Linux à partir de Linux</span><span class="sxs-lookup"><span data-stu-id="984b9-164">Accessing files in the Linux root file system from Linux</span></span>

<span data-ttu-id="984b9-165">Tous les fichiers créés, modifiés ou consultés dans le système de fichiers racine Linux suivent les conventions Linux standard, telles que l’application de l’umask à un fichier nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="984b9-165">Any files created, modified, or accessed in the Linux root file system follow standard Linux conventions, such as applying the umask to a newly created file.</span></span>

## <a name="configuring-file-permissions"></a><span data-ttu-id="984b9-166">Configuration des autorisations de fichier</span><span class="sxs-lookup"><span data-stu-id="984b9-166">Configuring file permissions</span></span>

<span data-ttu-id="984b9-167">Vous pouvez configurer vos autorisations de fichier à l’intérieur de vos lecteurs Windows à l’aide des options de montage dans WSL. conf.</span><span class="sxs-lookup"><span data-stu-id="984b9-167">You can configure your file permissions inside of your Windows drives using the mount options in wsl.conf.</span></span> <span data-ttu-id="984b9-168">Les options de montage vous permettent de définir des masques d’autorisations `umask`, `dmask` et `fmask`.</span><span class="sxs-lookup"><span data-stu-id="984b9-168">The mount options allow you to set `umask`, `dmask` and `fmask` permissions masks.</span></span> <span data-ttu-id="984b9-169">Le `umask` est appliqué à tous les fichiers, le `dmask` est appliqué uniquement aux répertoires et le `fmask` est appliqué uniquement aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="984b9-169">The `umask` is applied to all files, the `dmask` is applied just to directories and the `fmask` is applied just to files.</span></span> <span data-ttu-id="984b9-170">Ces masques d’autorisation sont ensuite placés via une opération OR logique lorsqu’ils sont appliqués aux fichiers. par exemple, si vous avez une valeur `umask` de `023` et une valeur `fmask` de `022`, le masque des autorisations résultant pour les fichiers sera `023`.</span><span class="sxs-lookup"><span data-stu-id="984b9-170">These permission masks are then put through a logical OR operation when being applied to files, e.g: If you have a `umask` value of `023` and an `fmask` value of `022` then the resulting permissions mask for files will be `023`.</span></span> 

<span data-ttu-id="984b9-171">Pour obtenir des instructions sur la procédure à suivre, consultez la page [« gérer les distributions Linux »](./wsl-config.md) .</span><span class="sxs-lookup"><span data-stu-id="984b9-171">Please see the ['Manage Linux Distributions'](./wsl-config.md) document page for instructions on how to do this.</span></span>
<!-- TODO: Add # to the link-->

