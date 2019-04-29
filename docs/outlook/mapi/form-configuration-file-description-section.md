---
title: フォーム構成ファイル [説明] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433095"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="3d596-103">フォーム構成ファイル [説明] セクション</span><span class="sxs-lookup"><span data-stu-id="3d596-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="3d596-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d596-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d596-105">**[Description]** セクションには、フォームのユーザーインターフェイスのコントロールに関連付けられているフォームのすべてのプロパティと、フォームの場所を特定するために使用される属性が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d596-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="3d596-106">フォームのメッセージクラスの名前、GUID、およびメッセージクラスの表示名を識別する**messageclass**、 **Clsid**、 **DisplayName**の各エントリは、フォームライブラリ内でフォームを検索するために使用される必須のエントリです。.</span><span class="sxs-lookup"><span data-stu-id="3d596-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="3d596-107">残りのエントリは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="3d596-107">The remaining entries are optional.</span></span> <span data-ttu-id="3d596-108">**[Description]** セクションの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3d596-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="3d596-109">**[Description]** セクションには、フォームのユーザーインターフェイスのコントロールに関連付けられているフォームのすべてのプロパティと、フォームの場所を特定するために使用される属性が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d596-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="3d596-110">フォームのメッセージクラスの名前、GUID、およびメッセージクラスの表示名を識別する**messageclass**、 **Clsid**、 **DisplayName**の各エントリは、フォームライブラリ内でフォームを検索するために使用される必須のエントリです。.</span><span class="sxs-lookup"><span data-stu-id="3d596-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="3d596-111">残りのエントリは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="3d596-111">The remaining entries are optional.</span></span> <span data-ttu-id="3d596-112">**[Description]** セクションの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3d596-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="3d596-113">**Descriptionmessageclass** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="3d596-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="3d596-114">**Clsid** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="3d596-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="3d596-115">**DisplayName** =  表示_文字列_</span><span class="sxs-lookup"><span data-stu-id="3d596-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="3d596-116">**SmallIcon** =  _パス_</span><span class="sxs-lookup"><span data-stu-id="3d596-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="3d596-117">**LargeIcon** =  _パス_</span><span class="sxs-lookup"><span data-stu-id="3d596-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="3d596-118">省略可能なエントリは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3d596-118">Optional entries are:</span></span>
  
 <span data-ttu-id="3d596-119">**カテゴリ** =  で_表示される文字列_</span><span class="sxs-lookup"><span data-stu-id="3d596-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="3d596-120">**サブカテゴリ** =  で_表示される文字列_</span><span class="sxs-lookup"><span data-stu-id="3d596-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="3d596-121">**コメント** =  の_表示文字列_</span><span class="sxs-lookup"><span data-stu-id="3d596-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="3d596-122">**所有者** =  が表示した_文字列_</span><span class="sxs-lookup"><span data-stu-id="3d596-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="3d596-123">**数値** =  で_表示される文字列_</span><span class="sxs-lookup"><span data-stu-id="3d596-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="3d596-124">**バージョン** =  _整数_</span><span class="sxs-lookup"><span data-stu-id="3d596-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="3d596-125">**ロケール** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="3d596-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="3d596-126">**非表示** =  の_整数_</span><span class="sxs-lookup"><span data-stu-id="3d596-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="3d596-127">**DesignerToolName** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="3d596-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="3d596-128">**デザイナツール guid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="3d596-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="3d596-129">**designerrアン timeguid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="3d596-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="3d596-130">**構成ファイル** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="3d596-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="3d596-131">**ComposeCommand** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="3d596-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="3d596-132">**カテゴリ**および**サブカテゴリ**のエントリは、フォームインストーラーによって使用され、クライアントアプリケーションのユーザーインターフェイス内のフォームの既定の分類を設定します。</span><span class="sxs-lookup"><span data-stu-id="3d596-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="3d596-133">たとえば、"Help Desk" がカテゴリで、"ソフトウェア" と "ハードウェア" がサブカテゴリである階層を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="3d596-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="3d596-134">この分類は、ビューアーアプリケーションで、より整理された方法でメッセージを表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="3d596-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="3d596-135">**コメント**、**所有者**、および**番号**エントリは、クライアントアプリケーションのユーザーインターフェイスに表示されるすべてのコメント文字列です。</span><span class="sxs-lookup"><span data-stu-id="3d596-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="3d596-136">フォーム開発者の裁量で使用できるフォーム固有のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="3d596-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="3d596-137">たとえば、**コメント**エントリを使用して、フォームの目的、フォームの管理を担当する個人または組織の指定に使用する**所有者**エントリ、およびフォームの異なるバージョンの追跡に使用される番号を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="3d596-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="3d596-138">**コメント**エントリでは、最大10行のコメントを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3d596-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="3d596-139">コメントの最初の行では、キーとして "Comment" という単語を使用し、2番目のコメントでは "Comment1" をキーとして使用し、次に "Comment9" を使用します。</span><span class="sxs-lookup"><span data-stu-id="3d596-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="3d596-140">**LargeIcon**および**SmallIcon**エントリは、クライアントアプリケーションのユーザーインターフェイスにアイコンを表示するために使用されるアイコンリソースのパスを指定するために使用されます。通常、これは、 **PR_ICON**を含むテーブル行用です ([PidTagIcon](pidtagicon-canonical-property.md))。or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティの列。</span><span class="sxs-lookup"><span data-stu-id="3d596-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="3d596-141">アイコンファイル名は、フォーム構成ファイルがインストールされているディレクトリを基準としたパス名として指定できます。</span><span class="sxs-lookup"><span data-stu-id="3d596-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="3d596-142">**バージョン**エントリは、フォームのバージョン番号を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d596-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="3d596-143">**ロケール**は、送信先フォームライブラリの3文字の言語識別子です。</span><span class="sxs-lookup"><span data-stu-id="3d596-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="3d596-144">これらの識別子の一覧については、 _Win32 プログラマーズリファレンスを参照_してください。</span><span class="sxs-lookup"><span data-stu-id="3d596-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="3d596-145">**非表示**のエントリは、フォームをフォームライブラリプロバイダのユーザーインターフェイスに表示するかどうかを示します。1は、ファイルが非表示になっていることを示し、0は、フォームが表示されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="3d596-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="3d596-146">フォーム構成ファイルの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3d596-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="3d596-147">構成\*\*\*\* するには、次のようにします。1は、ユーザーがメッセージを作成中に保存するときに、現在のフォルダーまたはユーザーの受信トレイにフォームを配置するように設計されているかどうかを制御します。1は、フォームが現在のフォルダーに移動することを示し、0は受信トレイに移動します。</span><span class="sxs-lookup"><span data-stu-id="3d596-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="3d596-148">**ComposeCommand** entry は、クライアントアプリケーションの [新規作成] メニューに配置される文字列です。</span><span class="sxs-lookup"><span data-stu-id="3d596-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="3d596-149">この引数を指定しない場合は、 **DisplayName**エントリが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d596-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
```cpp
[Description]
MessageClass = IPM.Help
Clsid = {00020D31-0000-0000-C000-000000000046}
DisplayName = Help Desk Request Form
;optional entries
Category = Help Desk Requests
Subcategory = New Requests
Comment = Use this form to request network assistance
Owner = Help Desk
Number = 1
SmallIcon = C:\WINDOWS|EFORMS\HELPDESK\HDSMALL.ICO
LargeIcon = C:\WINDOWS|EFORMS\HELPDESK\HDLARGE.ICO
Version = 1.00
Locale = enu
Hidden = 0
ComposeInFolder = 0
ComposeCommand = &Help Desk Request
 
```


