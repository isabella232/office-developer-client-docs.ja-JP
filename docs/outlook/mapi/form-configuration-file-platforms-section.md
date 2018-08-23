---
title: フォーム構成ファイル [Platforms] セクション
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ddc6db2303d9d5f114fdb27b6e15e699a04e73f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800099"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="8ad72-103">フォーム構成ファイル [Platforms] セクション</span><span class="sxs-lookup"><span data-stu-id="8ad72-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="8ad72-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ad72-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ad72-105">**[プラットフォーム]** セクションには、このフォームでサポートされているプラットフォームの完全なセットが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ad72-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="8ad72-106">プラットフォームの各エントリは、接頭辞**プラットフォームです**。</span><span class="sxs-lookup"><span data-stu-id="8ad72-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="8ad72-107">_文字列_、_文字列_は、プラットフォームには任意の文字列のコードをです。</span><span class="sxs-lookup"><span data-stu-id="8ad72-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="8ad72-108">各文字列は、個別の **[プラットフォーム]** セクションの**CPU**エントリに対応します。</span><span class="sxs-lookup"><span data-stu-id="8ad72-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="8ad72-109">**[プラットフォーム]** セクション内の各エントリは、それ以降を参照するための_プラットフォームの文字列_を定義 **[プラットフォームです**。</span><span class="sxs-lookup"><span data-stu-id="8ad72-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="8ad72-110">_プラットフォームの文字列_**]** のセクションで次のようにします。</span><span class="sxs-lookup"><span data-stu-id="8ad72-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="8ad72-111">**[プラットフォーム]** セクションには、このフォームでサポートされているプラットフォームの完全なセットが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ad72-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="8ad72-112">プラットフォームの各エントリは、接頭辞**プラットフォームです**。</span><span class="sxs-lookup"><span data-stu-id="8ad72-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="8ad72-113">_文字列_、_文字列_は、プラットフォームには任意の文字列のコードをです。</span><span class="sxs-lookup"><span data-stu-id="8ad72-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="8ad72-114">各文字列は、個別の **[プラットフォーム]** セクションの**CPU**エントリに対応します。</span><span class="sxs-lookup"><span data-stu-id="8ad72-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="8ad72-115">**[プラットフォーム]** セクション内の各エントリは、それ以降を参照するための_プラットフォームの文字列_を定義 **[プラットフォームです**。</span><span class="sxs-lookup"><span data-stu-id="8ad72-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="8ad72-116">_プラットフォームの文字列_**]** のセクションで次のようにします。</span><span class="sxs-lookup"><span data-stu-id="8ad72-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="8ad72-117">**[プラットフォーム]**</span><span class="sxs-lookup"><span data-stu-id="8ad72-117">**[Platforms]**</span></span>
  
<span data-ttu-id="8ad72-118">**プラットフォーム**です。</span><span class="sxs-lookup"><span data-stu-id="8ad72-118">**Platform**.</span></span> <span data-ttu-id="8ad72-119">_文字列_ =  _プラットフォームの文字列_</span><span class="sxs-lookup"><span data-stu-id="8ad72-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="8ad72-120">**[プラットフォーム]** セクションの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8ad72-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="8ad72-121">各 **[プラットフォームです**。</span><span class="sxs-lookup"><span data-stu-id="8ad72-121">Each **[Platform.**</span></span> <span data-ttu-id="8ad72-122">_プラットフォームの文字列_**]** ] セクションには、 **CPU** 、 **OSVersion**の 2 つの必要なエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8ad72-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="8ad72-123">**CPU**は、プロセッサを指定し、 **OSVersion**エントリは、オペレーティング システムを指定します。</span><span class="sxs-lookup"><span data-stu-id="8ad72-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="8ad72-124">**CPU**の有効な値については、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="8ad72-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="8ad72-125">**CPU エントリ**</span><span class="sxs-lookup"><span data-stu-id="8ad72-125">**CPU Entry**</span></span>|<span data-ttu-id="8ad72-126">**プロセッサ**</span><span class="sxs-lookup"><span data-stu-id="8ad72-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ad72-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="8ad72-127">Ix86</span></span>  <br/> |<span data-ttu-id="8ad72-128">Intel 80 x 86 Pentium シリーズのプロセッサと AMD、Cyrix、NextGen およびその他のメーカーから同等のプロセッサです。</span><span class="sxs-lookup"><span data-stu-id="8ad72-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="8ad72-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="8ad72-129">MIPS</span></span>  <br/> |<span data-ttu-id="8ad72-130">MIPS R4000 シリーズ ・ プロセッサです。</span><span class="sxs-lookup"><span data-stu-id="8ad72-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="8ad72-131">AXP</span><span class="sxs-lookup"><span data-stu-id="8ad72-131">AXP</span></span>  <br/> |<span data-ttu-id="8ad72-132">デジタル機器企業の Alpha AXP プロセッサです。</span><span class="sxs-lookup"><span data-stu-id="8ad72-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="8ad72-133">PPC</span><span class="sxs-lookup"><span data-stu-id="8ad72-133">PPC</span></span>  <br/> |<span data-ttu-id="8ad72-134">モトローラ社の Power PC シリーズ ・ プロセッサです。</span><span class="sxs-lookup"><span data-stu-id="8ad72-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="8ad72-135">M68</span><span class="sxs-lookup"><span data-stu-id="8ad72-135">M68</span></span>  <br/> |<span data-ttu-id="8ad72-136">Mororola 68 x 00 シリーズ ・ プロセッサです。</span><span class="sxs-lookup"><span data-stu-id="8ad72-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="8ad72-137">**OSVersion**の有効な値については、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="8ad72-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="8ad72-138">**OSVersion エントリ**</span><span class="sxs-lookup"><span data-stu-id="8ad72-138">**OSVersion Entry**</span></span>|<span data-ttu-id="8ad72-139">**オペレーティング システム**</span><span class="sxs-lookup"><span data-stu-id="8ad72-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ad72-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="8ad72-140">Win3.1</span></span>  <br/> |<span data-ttu-id="8ad72-141">Windows 3.1 および 3.11 をワークグループの Windows。</span><span class="sxs-lookup"><span data-stu-id="8ad72-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="8ad72-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="8ad72-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="8ad72-143">Windows NT 3.5 またはそれ以下では。</span><span class="sxs-lookup"><span data-stu-id="8ad72-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="8ad72-144">Win95</span><span class="sxs-lookup"><span data-stu-id="8ad72-144">Win95</span></span>  <br/> |<span data-ttu-id="8ad72-145">Windows 95 です。</span><span class="sxs-lookup"><span data-stu-id="8ad72-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="8ad72-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="8ad72-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="8ad72-147">Windows NT 4.0。</span><span class="sxs-lookup"><span data-stu-id="8ad72-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="8ad72-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="8ad72-148">Mac7</span></span>  <br/> |<span data-ttu-id="8ad72-149">Macintosh システム 7。</span><span class="sxs-lookup"><span data-stu-id="8ad72-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="8ad72-150">さらに、 **[プラットフォームです**。</span><span class="sxs-lookup"><span data-stu-id="8ad72-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="8ad72-151">_プラットフォームの文字列_**]** のセクションでは、**ファイル**または**リンク**のいずれかのエントリを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ad72-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="8ad72-152">**ファイル**のエントリは、フォーム サーバー アプリケーション実行可能ファイル、フォーム ライブラリを維持し、フォームを起動すると、ディスク キャッシュに新しいサブディレクトリにロードを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8ad72-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="8ad72-153">**リンク**エントリを代わりに使用する場合、**ファイル**情報の取得元となるプラットフォームのさまざまな文字列の名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8ad72-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="8ad72-154">これは、フォームの 1 つのバージョンには、複数のプラットフォームがサポートしている場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="8ad72-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="8ad72-155">**ファイル**のエントリが使用されるたびに、**レジストリ**エントリが使用される、フォームのサーバー アプリケーションの実行可能ファイルが保存されているフォーム ライブラリのレジストリ キーを識別します。</span><span class="sxs-lookup"><span data-stu-id="8ad72-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="8ad72-156">円記号 (\) に続く文字列は、レジストリのルートに配置されます。</span><span class="sxs-lookup"><span data-stu-id="8ad72-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="8ad72-157">いない円記号に続く文字列が_GUID_の HKEY_CLASSES_ROOT\CLSID\ に配置されます。 _GUID_は、フォームの**GUID**のレジストリ キーです。</span><span class="sxs-lookup"><span data-stu-id="8ad72-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="8ad72-158">"%D"の文字は、フォーム構成ファイルの読み取り元のディレクトリのパス名を示すために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8ad72-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="8ad72-159">これは、機能は、フォーム構成ファイルへの相対パス名とその他のファイルを指定するために便利です。</span><span class="sxs-lookup"><span data-stu-id="8ad72-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="8ad72-160">その他のテキストの後にプレフィックスとして、ファイルまたはレジストリを使用して**複数のファイル**または**レジストリ**エントリを指定できます。</span><span class="sxs-lookup"><span data-stu-id="8ad72-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="8ad72-161">形式、 **[プラットフォームです**。</span><span class="sxs-lookup"><span data-stu-id="8ad72-161">The format for the **[Platform.**</span></span> <span data-ttu-id="8ad72-162">_プラットフォームの文字列_**]** のセクションでは。</span><span class="sxs-lookup"><span data-stu-id="8ad72-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="8ad72-163">**[プラットフォームです。**</span><span class="sxs-lookup"><span data-stu-id="8ad72-163">**[Platform.**</span></span> <span data-ttu-id="8ad72-164">_プラットフォームの文字列_**]**</span><span class="sxs-lookup"><span data-stu-id="8ad72-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="8ad72-165">**CPU** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="8ad72-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="8ad72-166">**OSVersion** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="8ad72-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="8ad72-167">**ファイル** =  _のパス_</span><span class="sxs-lookup"><span data-stu-id="8ad72-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="8ad72-168">**リンク** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="8ad72-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="8ad72-169">**レジストリ** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="8ad72-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="8ad72-170">2 つの例を次に示します **[プラットフォームです**。</span><span class="sxs-lookup"><span data-stu-id="8ad72-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="8ad72-171">_プラットフォームの文字列_**]** のセクション**ファイル**のエントリを使用して、**リンク**のエントリを使用します。</span><span class="sxs-lookup"><span data-stu-id="8ad72-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="8ad72-172">**[プラットフォームです**。</span><span class="sxs-lookup"><span data-stu-id="8ad72-172">The **[Platform.**</span></span> <span data-ttu-id="8ad72-173">_プラットフォームの文字列_**]** のセクションでは、インストーラーが利用可能なローカル ストレージに OLE レジストリにハンドラーの名前とメッセージ クラスのハンドラーを構成するファイルを配置しているし、行ったことが前提とすると、ローカルのフォーム ライブラリにフォームを追加するときに無視されますがシステムのレジストリ内の OLE 登録します。</span><span class="sxs-lookup"><span data-stu-id="8ad72-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

