---
title: フォーム構成ファイル [プラットフォーム] セクション
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327511"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="e6e60-103">フォーム構成ファイル [プラットフォーム] セクション</span><span class="sxs-lookup"><span data-stu-id="e6e60-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="e6e60-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6e60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6e60-105">**[プラットフォーム]** セクションには、このフォームでサポートされているプラットフォームの完全なセットが一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="e6e60-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="e6e60-106">各プラットフォームエントリは、プレフィックスプラットフォームで構成さ**れています。**</span><span class="sxs-lookup"><span data-stu-id="e6e60-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="e6e60-107">__ string。 _string_は、プラットフォームの任意の文字列コードです。</span><span class="sxs-lookup"><span data-stu-id="e6e60-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="e6e60-108">各文字列は、個々の **[プラットフォーム]** セクションの**CPU**エントリに対応します。</span><span class="sxs-lookup"><span data-stu-id="e6e60-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="e6e60-109">**[platform]** セクションの各エントリは、以降の [プラットフォーム] を参照する_プラットフォーム文字列_を定義し**ます。**</span><span class="sxs-lookup"><span data-stu-id="e6e60-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="e6e60-110">_プラットフォーム文字列_**]** セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6e60-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="e6e60-111">**[プラットフォーム]** セクションには、このフォームでサポートされているプラットフォームの完全なセットが一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="e6e60-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="e6e60-112">各プラットフォームエントリは、プレフィックスプラットフォームで構成さ**れています。**</span><span class="sxs-lookup"><span data-stu-id="e6e60-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="e6e60-113">__ string。 _string_は、プラットフォームの任意の文字列コードです。</span><span class="sxs-lookup"><span data-stu-id="e6e60-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="e6e60-114">各文字列は、個々の **[プラットフォーム]** セクションの**CPU**エントリに対応します。</span><span class="sxs-lookup"><span data-stu-id="e6e60-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="e6e60-115">**[platform]** セクションの各エントリは、以降の [プラットフォーム] を参照する_プラットフォーム文字列_を定義し**ます。**</span><span class="sxs-lookup"><span data-stu-id="e6e60-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="e6e60-116">_プラットフォーム文字列_**]** セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6e60-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="e6e60-117">**対象**</span><span class="sxs-lookup"><span data-stu-id="e6e60-117">**[Platforms]**</span></span>
  
<span data-ttu-id="e6e60-118">**プラットフォーム**。</span><span class="sxs-lookup"><span data-stu-id="e6e60-118">**Platform**.</span></span> <span data-ttu-id="e6e60-119">_文字列_ =  _プラットフォーム文字列_</span><span class="sxs-lookup"><span data-stu-id="e6e60-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="e6e60-120">**[プラットフォーム]** セクションの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e6e60-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="e6e60-121">各 **[プラットフォーム**</span><span class="sxs-lookup"><span data-stu-id="e6e60-121">Each **[Platform.**</span></span> <span data-ttu-id="e6e60-122">_プラットフォーム文字列_**]** セクションには、2つの必須のエントリ、 **CPU** 、および**OSVersion**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e6e60-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="e6e60-123">**cpu**エントリはプロセッサを指定し、 **OSVersion**エントリはオペレーティングシステムを指定します。</span><span class="sxs-lookup"><span data-stu-id="e6e60-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="e6e60-124">次の表では、有効な**CPU**の値について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6e60-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="e6e60-125">**CPU エントリ**</span><span class="sxs-lookup"><span data-stu-id="e6e60-125">**CPU Entry**</span></span>|<span data-ttu-id="e6e60-126">**プロセッサ**</span><span class="sxs-lookup"><span data-stu-id="e6e60-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6e60-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="e6e60-127">Ix86</span></span>  <br/> |<span data-ttu-id="e6e60-128">Intel 80x86 および Pentium シリーズプロセッサ、および AMD、Cyrix、nextgen およびその他の製造元の同等のプロセッサ。</span><span class="sxs-lookup"><span data-stu-id="e6e60-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="e6e60-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="e6e60-129">MIPS</span></span>  <br/> |<span data-ttu-id="e6e60-130">MIPS R4000 series プロセッサ。</span><span class="sxs-lookup"><span data-stu-id="e6e60-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="e6e60-131">AXP</span><span class="sxs-lookup"><span data-stu-id="e6e60-131">AXP</span></span>  <br/> |<span data-ttu-id="e6e60-132">デジタル機器 Corporation Alpha AXP プロセッサ。</span><span class="sxs-lookup"><span data-stu-id="e6e60-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="e6e60-133">PPC</span><span class="sxs-lookup"><span data-stu-id="e6e60-133">PPC</span></span>  <br/> |<span data-ttu-id="e6e60-134">Motorola Power PC series プロセッサ。</span><span class="sxs-lookup"><span data-stu-id="e6e60-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="e6e60-135">M68</span><span class="sxs-lookup"><span data-stu-id="e6e60-135">M68</span></span>  <br/> |<span data-ttu-id="e6e60-136">Mororola 68x00 series プロセッサ。</span><span class="sxs-lookup"><span data-stu-id="e6e60-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="e6e60-137">次の表では、有効な**OSVersion**の値について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6e60-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="e6e60-138">**OSVersion エントリ**</span><span class="sxs-lookup"><span data-stu-id="e6e60-138">**OSVersion Entry**</span></span>|<span data-ttu-id="e6e60-139">**オペレーティング システム**</span><span class="sxs-lookup"><span data-stu-id="e6e60-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6e60-140">win 3.1</span><span class="sxs-lookup"><span data-stu-id="e6e60-140">Win3.1</span></span>  <br/> |<span data-ttu-id="e6e60-141">windows 3.1 および windows for ワークグループ3.11。</span><span class="sxs-lookup"><span data-stu-id="e6e60-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="e6e60-142">winnt 3.5</span><span class="sxs-lookup"><span data-stu-id="e6e60-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="e6e60-143">Windows NT 3.5 またはそれ以降。</span><span class="sxs-lookup"><span data-stu-id="e6e60-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="e6e60-144">95</span><span class="sxs-lookup"><span data-stu-id="e6e60-144">Win95</span></span>  <br/> |<span data-ttu-id="e6e60-145">Windows 95。</span><span class="sxs-lookup"><span data-stu-id="e6e60-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="e6e60-146">winnt 4.0</span><span class="sxs-lookup"><span data-stu-id="e6e60-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="e6e60-147">Windows NT 4.0。</span><span class="sxs-lookup"><span data-stu-id="e6e60-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="e6e60-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="e6e60-148">Mac7</span></span>  <br/> |<span data-ttu-id="e6e60-149">Macintosh システム7。</span><span class="sxs-lookup"><span data-stu-id="e6e60-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="e6e60-150">また、 **[プラットフォーム**]</span><span class="sxs-lookup"><span data-stu-id="e6e60-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="e6e60-151">_プラットフォーム文字列_**]** セクションには、 **File**または**linkto** entry のいずれかを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6e60-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="e6e60-152">**ファイル**エントリには、フォームライブラリが保持するフォームサーバーアプリケーションの実行可能ファイルがリストされており、フォームの起動時にディスクキャッシュ内の新しいサブディレクトリに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="e6e60-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="e6e60-153">代わりに、 **linkto**エントリが使用されている場合は、**ファイル**情報を取得する別のプラットフォーム文字列の名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e6e60-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="e6e60-154">これは、フォームの1つのバージョンが複数のプラットフォームをサポートしている場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="e6e60-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="e6e60-155">**レジストリ**エントリは、**ファイル**エントリが使用されるたびに使用され、フォームサーバーアプリケーションの実行可能ファイルが格納されているフォームライブラリのレジストリキーを識別します。</span><span class="sxs-lookup"><span data-stu-id="e6e60-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="e6e60-156">円記号 (\) の後に続く文字列は、レジストリのルートに配置されます。</span><span class="sxs-lookup"><span data-stu-id="e6e60-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="e6e60-157">先頭に円記号を付けない文字列は、HKEY_CLASSES_ROOT\CLSID\ _GUID_\ レジストリキーに配置されます。 _guid_はフォームの**guid**です。</span><span class="sxs-lookup"><span data-stu-id="e6e60-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="e6e60-158">文字 "% d" は、フォーム構成ファイルが読み取られたディレクトリのパス名を示すために使用できます。</span><span class="sxs-lookup"><span data-stu-id="e6e60-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="e6e60-159">これは、フォーム構成ファイルを基準としたパス名を持つ他のファイルを指定する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="e6e60-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="e6e60-160">ファイルまたはレジストリをプレフィックスとして使用し、他のテキストを続けて指定することで、**複数のファイル**または**レジストリ**エントリを指定できます。</span><span class="sxs-lookup"><span data-stu-id="e6e60-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="e6e60-161">**[プラットフォーム**] の形式。</span><span class="sxs-lookup"><span data-stu-id="e6e60-161">The format for the **[Platform.**</span></span> <span data-ttu-id="e6e60-162">_プラットフォーム文字列_**]** セクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e6e60-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="e6e60-163">**プラットフォーム.**</span><span class="sxs-lookup"><span data-stu-id="e6e60-163">**[Platform.**</span></span> <span data-ttu-id="e6e60-164">_プラットフォーム文字列_**]**</span><span class="sxs-lookup"><span data-stu-id="e6e60-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="e6e60-165">**CPU** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="e6e60-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="e6e60-166">**OSVersion** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="e6e60-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="e6e60-167">**ファイル** =  _パス_</span><span class="sxs-lookup"><span data-stu-id="e6e60-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="e6e60-168">**linkto** =  _string_</span><span class="sxs-lookup"><span data-stu-id="e6e60-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="e6e60-169">**レジストリ** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="e6e60-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="e6e60-170">次に2つの例を示し**ます (Platform)。**</span><span class="sxs-lookup"><span data-stu-id="e6e60-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="e6e60-171">_プラットフォーム文字列_**]** セクション。1つは**ファイル**エントリを使用し、もう1つは**linkto**エントリを使用します。</span><span class="sxs-lookup"><span data-stu-id="e6e60-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

<span data-ttu-id="e6e60-172">**[プラットフォーム.**</span><span class="sxs-lookup"><span data-stu-id="e6e60-172">The **[Platform.**</span></span> <span data-ttu-id="e6e60-173">_プラットフォーム文字列_**] []** セクションは、ローカルフォームライブラリにフォームを追加するときには無視されます。これは、インストーラーが、OLE レジストリのハンドラーのセクションで指定されているように、使用可能なローカル記憶域にメッセージクラスハンドラーを設定したファイルを配置したと仮定した場合です。システムのレジストリに登録されている OLE。</span><span class="sxs-lookup"><span data-stu-id="e6e60-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

