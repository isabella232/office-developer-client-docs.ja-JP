---
title: フォーム構成ファイル [プラットフォーム] セクション
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419129"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="466db-103">フォーム構成ファイル [プラットフォーム] セクション</span><span class="sxs-lookup"><span data-stu-id="466db-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="466db-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="466db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="466db-105">[ **プラットフォーム] セクションには** 、このフォームでサポートされているプラットフォームの完全なセットが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="466db-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="466db-106">各プラットフォーム エントリは、プレフィックス **Platform で構成されます。**</span><span class="sxs-lookup"><span data-stu-id="466db-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="466db-107">_string_ は  _プラットフォーム_ の任意の文字列コードです。</span><span class="sxs-lookup"><span data-stu-id="466db-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="466db-108">各文字列は、個々の **[プラットフォーム** ] セクションの **CPU エントリに** 対応します。</span><span class="sxs-lookup"><span data-stu-id="466db-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="466db-109">[プラットフォーム]**セクションの各エントリは**、後続の[プラットフォーム] を参照するプラットフォーム文字列 **を定義します。**</span><span class="sxs-lookup"><span data-stu-id="466db-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="466db-110">_次に示すように_**、** プラットフォーム文字列 ] セクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="466db-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="466db-111">[ **プラットフォーム] セクションには** 、このフォームでサポートされているプラットフォームの完全なセットが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="466db-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="466db-112">各プラットフォーム エントリは、プレフィックス **Platform で構成されます。**</span><span class="sxs-lookup"><span data-stu-id="466db-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="466db-113">_string_ は  _プラットフォーム_ の任意の文字列コードです。</span><span class="sxs-lookup"><span data-stu-id="466db-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="466db-114">各文字列は、個々の **[プラットフォーム** ] セクションの **CPU エントリに** 対応します。</span><span class="sxs-lookup"><span data-stu-id="466db-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="466db-115">[プラットフォーム]**セクションの各エントリは**、後続の[プラットフォーム] を参照するプラットフォーム文字列 **を定義します。**</span><span class="sxs-lookup"><span data-stu-id="466db-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="466db-116">_次に示すように_**、** プラットフォーム文字列 ] セクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="466db-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="466db-117">**[プラットフォーム]**</span><span class="sxs-lookup"><span data-stu-id="466db-117">**[Platforms]**</span></span>
  
<span data-ttu-id="466db-118">**プラットフォーム**.</span><span class="sxs-lookup"><span data-stu-id="466db-118">**Platform**.</span></span> <span data-ttu-id="466db-119">_string_  =  _プラットフォーム文字列_</span><span class="sxs-lookup"><span data-stu-id="466db-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="466db-120">[プラットフォーム] セクションの **例を次に示** します。</span><span class="sxs-lookup"><span data-stu-id="466db-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="466db-121">各 **[プラットフォーム]**</span><span class="sxs-lookup"><span data-stu-id="466db-121">Each **[Platform.**</span></span> <span data-ttu-id="466db-122">_プラットフォーム文字列_ **] セクション** には、CPU と **OSVersion** の 2 つの必須 **エントリが含まれます**。</span><span class="sxs-lookup"><span data-stu-id="466db-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="466db-123">**CPU エントリ** はプロセッサを指定し **、OSVersion** エントリはオペレーティング システムを指定します。</span><span class="sxs-lookup"><span data-stu-id="466db-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="466db-124">有効 **な CPU** 値については、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="466db-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="466db-125">**CPU エントリ**</span><span class="sxs-lookup"><span data-stu-id="466db-125">**CPU Entry**</span></span>|<span data-ttu-id="466db-126">**プロセッサ**</span><span class="sxs-lookup"><span data-stu-id="466db-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="466db-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="466db-127">Ix86</span></span>  <br/> |<span data-ttu-id="466db-128">Intel 80x86 および Pentium シリーズ プロセッサ、AMD、Cyrix、NextGen、その他のメーカーの同等のプロセッサ。</span><span class="sxs-lookup"><span data-stu-id="466db-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="466db-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="466db-129">MIPS</span></span>  <br/> |<span data-ttu-id="466db-130">MIPS R4000 シリーズ プロセッサ。</span><span class="sxs-lookup"><span data-stu-id="466db-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="466db-131">AXP</span><span class="sxs-lookup"><span data-stu-id="466db-131">AXP</span></span>  <br/> |<span data-ttu-id="466db-132">Digital Equipment Corporation Alpha AXP プロセッサ。</span><span class="sxs-lookup"><span data-stu-id="466db-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="466db-133">PPC</span><span class="sxs-lookup"><span data-stu-id="466db-133">PPC</span></span>  <br/> |<span data-ttu-id="466db-134">Motorola Power PC シリーズ プロセッサ。</span><span class="sxs-lookup"><span data-stu-id="466db-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="466db-135">M68</span><span class="sxs-lookup"><span data-stu-id="466db-135">M68</span></span>  <br/> |<span data-ttu-id="466db-136">Mororola 68x00 シリーズ プロセッサ。</span><span class="sxs-lookup"><span data-stu-id="466db-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="466db-137">有効 **な OSVersion** 値については、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="466db-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="466db-138">**OSVersion エントリ**</span><span class="sxs-lookup"><span data-stu-id="466db-138">**OSVersion Entry**</span></span>|<span data-ttu-id="466db-139">**オペレーティング システム**</span><span class="sxs-lookup"><span data-stu-id="466db-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="466db-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="466db-140">Win3.1</span></span>  <br/> |<span data-ttu-id="466db-141">Windows 3.1 および Windows 3.11 の場合。</span><span class="sxs-lookup"><span data-stu-id="466db-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="466db-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="466db-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="466db-143">Windows NT 3.5 以下。</span><span class="sxs-lookup"><span data-stu-id="466db-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="466db-144">Win95</span><span class="sxs-lookup"><span data-stu-id="466db-144">Win95</span></span>  <br/> |<span data-ttu-id="466db-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="466db-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="466db-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="466db-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="466db-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="466db-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="466db-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="466db-148">Mac7</span></span>  <br/> |<span data-ttu-id="466db-149">Macintosh System 7.</span><span class="sxs-lookup"><span data-stu-id="466db-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="466db-150">さらに、[ **プラットフォーム] を使用します。**</span><span class="sxs-lookup"><span data-stu-id="466db-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="466db-151">_プラットフォーム文字列_ **] セクション** には、File エントリまたは LinkTo エントリ **が含まれている必要** があります。</span><span class="sxs-lookup"><span data-stu-id="466db-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="466db-152">[ **ファイル]** エントリには、フォーム ライブラリが保持するフォーム サーバー アプリケーション実行可能ファイルが一覧表示され、フォームの起動時にディスク キャッシュ内の新しいサブディレクトリに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="466db-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="466db-153">代わりに **LinkTo** エントリを使用する場合は、ファイル情報を取得する別のプラットフォーム文字列 **の名前が** 含まれます。</span><span class="sxs-lookup"><span data-stu-id="466db-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="466db-154">これは、1 つのバージョンのフォームが複数のプラットフォームをサポートしている場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="466db-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="466db-155">レジストリ **エントリは** 、 **ファイル** エントリが使用されるたびに使用され、フォーム サーバー アプリケーションの実行可能ファイルが格納されているフォーム ライブラリのレジストリ キーを識別します。</span><span class="sxs-lookup"><span data-stu-id="466db-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="466db-156">バックスラッシュ ( \ ) が先行する文字列は、レジストリのルートに配置されます。</span><span class="sxs-lookup"><span data-stu-id="466db-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="466db-157">バックスラッシュの前に文字列が置かHKEY_CLASSES_ROOT\CLSID\  _GUID_\ レジストリ キー  _、GUID_ は、フォームの **GUID** です。</span><span class="sxs-lookup"><span data-stu-id="466db-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="466db-158">"%d" という文字を使用して、フォーム構成ファイルの読み取りが開始されたディレクトリのパス名を示します。</span><span class="sxs-lookup"><span data-stu-id="466db-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="466db-159">これは、フォーム構成ファイルを基準にパス名を持つ他のファイルを指定する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="466db-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="466db-160">**ファイルまたはレジストリ** の **複数のエントリ** は、プレフィックスとして File または Registry を使用し、その後に他のテキストを付け、指定できます。</span><span class="sxs-lookup"><span data-stu-id="466db-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="466db-161">[プラットフォーム] **の形式。**</span><span class="sxs-lookup"><span data-stu-id="466db-161">The format for the **[Platform.**</span></span> <span data-ttu-id="466db-162">_プラットフォーム文字列_ **] セクション** は次の場合です。</span><span class="sxs-lookup"><span data-stu-id="466db-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="466db-163">**[プラットフォーム]**</span><span class="sxs-lookup"><span data-stu-id="466db-163">**[Platform.**</span></span> <span data-ttu-id="466db-164">_プラットフォーム文字列_ **]**</span><span class="sxs-lookup"><span data-stu-id="466db-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="466db-165">**CPU**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="466db-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="466db-166">**OSVersion**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="466db-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="466db-167">**ファイル**  =  _path_</span><span class="sxs-lookup"><span data-stu-id="466db-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="466db-168">**LinkTo**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="466db-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="466db-169">**レジストリ**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="466db-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="466db-170">[プラットフォーム] の 2 **つの例を次に示します。**</span><span class="sxs-lookup"><span data-stu-id="466db-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="466db-171">_プラットフォーム文字列_ **] セクション** 。1 つは **File** エントリを使用し、もう 1 つは **LinkTo エントリを使用** します。</span><span class="sxs-lookup"><span data-stu-id="466db-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="466db-172">**[プラットフォーム]**</span><span class="sxs-lookup"><span data-stu-id="466db-172">The **[Platform.**</span></span> <span data-ttu-id="466db-173">_ローカル_ フォーム ライブラリにフォームを追加する場合、プラットフォーム文字列 **]** セクションは無視されます。インストーラーは、メッセージ クラス ハンドラーを構成するファイルを OLE レジストリのハンドラーのセクションで指定された利用可能なローカル ストレージに配置し、システムのレジストリで OLE 登録を行ったと仮定します。</span><span class="sxs-lookup"><span data-stu-id="466db-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

