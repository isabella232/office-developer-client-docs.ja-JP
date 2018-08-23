---
title: フォーム構成ファイル [Description] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d3673c3b10afb55121339e335163ce9b2e5937e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800086"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="48ae7-103">フォーム構成ファイル [Description] セクション</span><span class="sxs-lookup"><span data-stu-id="48ae7-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="48ae7-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48ae7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48ae7-105">**[説明]** セクションには、フォームのコントロールでは、[フォームのユーザー インターフェイスでは、フォームの検索に使用される属性に関連付けられているすべてのプロパティが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="48ae7-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="48ae7-106">**MessageClass**、 **Clsid**、および**表示名**のエントリは、フォームのメッセージ クラス、その GUID、およびメッセージ クラスの表示名の名前をそれぞれ識別するには、フォーム ライブラリ内でフォームを検索するため、必要なエントリをします。.</span><span class="sxs-lookup"><span data-stu-id="48ae7-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="48ae7-107">残りのエントリはオプションです。</span><span class="sxs-lookup"><span data-stu-id="48ae7-107">The remaining entries are optional.</span></span> <span data-ttu-id="48ae7-108">**[説明]** セクションの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="48ae7-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="48ae7-109">**[説明]** セクションには、フォームのコントロールでは、[フォームのユーザー インターフェイスでは、フォームの検索に使用される属性に関連付けられているすべてのプロパティが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="48ae7-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="48ae7-110">**MessageClass**、 **Clsid**、および**表示名**のエントリは、フォームのメッセージ クラス、その GUID、およびメッセージ クラスの表示名の名前をそれぞれ識別するには、フォーム ライブラリ内でフォームを検索するため、必要なエントリをします。.</span><span class="sxs-lookup"><span data-stu-id="48ae7-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="48ae7-111">残りのエントリはオプションです。</span><span class="sxs-lookup"><span data-stu-id="48ae7-111">The remaining entries are optional.</span></span> <span data-ttu-id="48ae7-112">**[説明]** セクションの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="48ae7-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="48ae7-113">**[説明]MessageClass** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="48ae7-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="48ae7-114">**Clsid** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="48ae7-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="48ae7-115">**表示名** =  _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="48ae7-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="48ae7-116">**SmallIcon** =  _のパス_</span><span class="sxs-lookup"><span data-stu-id="48ae7-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="48ae7-117">**LargeIcon** =  _のパス_</span><span class="sxs-lookup"><span data-stu-id="48ae7-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="48ae7-118">省略可能なエントリは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="48ae7-118">Optional entries are:</span></span>
  
 <span data-ttu-id="48ae7-119">**カテゴリ** =  _の文字列が表示されます_</span><span class="sxs-lookup"><span data-stu-id="48ae7-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="48ae7-120">**サブカテゴリ** =  _の文字列が表示されます_</span><span class="sxs-lookup"><span data-stu-id="48ae7-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="48ae7-121">**コメント** =  _の文字列が表示されます_</span><span class="sxs-lookup"><span data-stu-id="48ae7-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="48ae7-122">**所有者** =  _の文字列が表示されます_</span><span class="sxs-lookup"><span data-stu-id="48ae7-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="48ae7-123">**数** =  _の文字列が表示されます_</span><span class="sxs-lookup"><span data-stu-id="48ae7-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="48ae7-124">**バージョン** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="48ae7-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="48ae7-125">**ロケール** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="48ae7-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="48ae7-126">**非表示** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="48ae7-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="48ae7-127">**DesignerToolName** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="48ae7-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="48ae7-128">**DesignerToolGuid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="48ae7-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="48ae7-129">**DesignerRuntimeGuid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="48ae7-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="48ae7-130">**ComposeInFolder** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="48ae7-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="48ae7-131">**ComposeCommand** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="48ae7-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="48ae7-132">**カテゴリ**と**サブカテゴリ**のエントリは、クライアント アプリケーションのユーザー インターフェイス内のフォームの既定の分類を設定するのには、フォームのインストーラーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="48ae7-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="48ae7-133">などの階層が設定するカテゴリの「ヘルプデスク」のある、「ソフトウェア」および「ハードウェア」サブカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="48ae7-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="48ae7-134">この分類より整理された形でメッセージを表示するビューアーのアプリケーションで使用できます。</span><span class="sxs-lookup"><span data-stu-id="48ae7-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="48ae7-135">**コメント**、**所有者**、および**番号**のエントリは、クライアント アプリケーションのユーザー インターフェイスに表示されるすべてのコメント文字列です。</span><span class="sxs-lookup"><span data-stu-id="48ae7-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="48ae7-136">これらは、フォームの開発者の裁量で使用できるフォーム固有のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="48ae7-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="48ae7-137">たとえば、フォーム、人や、フォームの管理を担当する組織を指定するための**所有者**のエントリと、フォームの別のバージョンを追跡するための番号の目的を示すために**コメント**の入力を使用できます。</span><span class="sxs-lookup"><span data-stu-id="48ae7-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="48ae7-138">**コメント**のコメントの 10 行までのエントリを含めることできます。</span><span class="sxs-lookup"><span data-stu-id="48ae7-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="48ae7-139">コメントの最初の行では、「コメント」という単語を使用して、キーとして、コメントの 2 行目が"Comment9"にしますを通じてというようにキーとして"Comment1"を使用して</span><span class="sxs-lookup"><span data-stu-id="48ae7-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="48ae7-140">**LargeIcon** 、 **SmallIcon**エントリ アイコンを表示するクライアント アプリケーションのユーザー インターフェイスで使用されるアイコン リソースへのパスを指定するため、通常これは、 **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) を含むテーブルの行または**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) のプロパティの列を選択します。</span><span class="sxs-lookup"><span data-stu-id="48ae7-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="48ae7-141">アイコンのファイル名は、フォーム構成ファイルがインストールされているディレクトリからの相対パス名として指定できます。</span><span class="sxs-lookup"><span data-stu-id="48ae7-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="48ae7-142">**バージョン**エントリを使用して、フォームのバージョン番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="48ae7-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="48ae7-143">**ロケール**は、移動先のフォーム ライブラリの 3 文字の言語識別子です。</span><span class="sxs-lookup"><span data-stu-id="48ae7-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="48ae7-144">これらの識別子の一覧については、 _Win32 プログラマーズ リファレンス_を参照しています。</span><span class="sxs-lookup"><span data-stu-id="48ae7-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="48ae7-145">**隠し**エントリは、フォームをフォーム ライブラリ プロバイダーのユーザー インターフェイスに表示かどうかを示します: 1 ことを示し、ファイルが隠しファイル 0 は、フォームが表示されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="48ae7-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="48ae7-146">次のフォーム構成ファイルの例が表示されます。</span><span class="sxs-lookup"><span data-stu-id="48ae7-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="48ae7-147">**ComposeInFolder**エントリは、フォームにユーザーがそれを作成するときにメッセージを保存すると、現在のフォルダーまたはユーザーの受信トレイに配置するよう設計されて かどうかを制御: 1 ことを示し、フォームが現在のフォルダーに移動する必要があります必要がある場合は 0受信トレイに移動します。</span><span class="sxs-lookup"><span data-stu-id="48ae7-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="48ae7-148">**ComposeCommand**エントリは、クライアント アプリケーションに格納する文字列は、メニューを作成のです。</span><span class="sxs-lookup"><span data-stu-id="48ae7-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="48ae7-149">これを指定しない場合は、**表示名**のエントリが使用されます。</span><span class="sxs-lookup"><span data-stu-id="48ae7-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


