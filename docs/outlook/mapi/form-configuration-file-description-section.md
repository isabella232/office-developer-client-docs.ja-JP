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
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="054d5-103">フォーム構成ファイル [説明] セクション</span><span class="sxs-lookup"><span data-stu-id="054d5-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="054d5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="054d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="054d5-105">**[説明] セクションには**、フォームのユーザー インターフェイスのコントロールに関連付けられているフォームのすべてのプロパティと、フォームの検索に使用される属性が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="054d5-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="054d5-106">フォーム のメッセージ クラスの名前、GUID、およびメッセージ クラスの表示名をそれぞれ識別する MessageClass、Clsid、**および DisplayName** エントリは、フォーム ライブラリ内でフォームを検索するために使用される必須エントリです。  </span><span class="sxs-lookup"><span data-stu-id="054d5-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="054d5-107">残りのエントリはオプションです。</span><span class="sxs-lookup"><span data-stu-id="054d5-107">The remaining entries are optional.</span></span> <span data-ttu-id="054d5-108">[説明] セクション **の形式は** 次の形式です。</span><span class="sxs-lookup"><span data-stu-id="054d5-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="054d5-109">**[説明] セクションには**、フォームのユーザー インターフェイスのコントロールに関連付けられているフォームのすべてのプロパティと、フォームの検索に使用される属性が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="054d5-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="054d5-110">フォーム のメッセージ クラスの名前、GUID、およびメッセージ クラスの表示名をそれぞれ識別する MessageClass、Clsid、**および DisplayName** エントリは、フォーム ライブラリ内でフォームを検索するために使用される必須エントリです。  </span><span class="sxs-lookup"><span data-stu-id="054d5-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="054d5-111">残りのエントリはオプションです。</span><span class="sxs-lookup"><span data-stu-id="054d5-111">The remaining entries are optional.</span></span> <span data-ttu-id="054d5-112">[説明] セクション **の形式は** 次の形式です。</span><span class="sxs-lookup"><span data-stu-id="054d5-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="054d5-113">**[説明] MessageClass**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="054d5-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="054d5-114">**Clsid**  =  _guid_</span><span class="sxs-lookup"><span data-stu-id="054d5-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="054d5-115">**DisplayName**  =  _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="054d5-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="054d5-116">**SmallIcon**  =  _path_</span><span class="sxs-lookup"><span data-stu-id="054d5-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="054d5-117">**LargeIcon**  =  _path_</span><span class="sxs-lookup"><span data-stu-id="054d5-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="054d5-118">オプションのエントリは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="054d5-118">Optional entries are:</span></span>
  
 <span data-ttu-id="054d5-119">**カテゴリ**  =  _表示される文字列_</span><span class="sxs-lookup"><span data-stu-id="054d5-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="054d5-120">**Subcategory**  =  _表示される文字列_</span><span class="sxs-lookup"><span data-stu-id="054d5-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="054d5-121">**コメント**  =  _表示される文字列_</span><span class="sxs-lookup"><span data-stu-id="054d5-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="054d5-122">**所有者**  =  _表示される文字列_</span><span class="sxs-lookup"><span data-stu-id="054d5-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="054d5-123">**数値**  =  _表示される文字列_</span><span class="sxs-lookup"><span data-stu-id="054d5-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="054d5-124">**バージョン**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="054d5-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="054d5-125">**ロケール**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="054d5-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="054d5-126">**非表示**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="054d5-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="054d5-127">**DesignerToolName**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="054d5-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="054d5-128">**DesignerToolGuid**  =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="054d5-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="054d5-129">**DesignerRuntimeGuid**  =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="054d5-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="054d5-130">**ComposeInFolder**  =  _0|1_</span><span class="sxs-lookup"><span data-stu-id="054d5-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="054d5-131">**ComposeCommand**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="054d5-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="054d5-132">Category **エントリ** と **Subcategory エントリ** は、フォーム インストーラーによって使用され、クライアント アプリケーションのユーザー インターフェイス内でフォームの既定の分類を設定します。</span><span class="sxs-lookup"><span data-stu-id="054d5-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="054d5-133">たとえば、"Help Desk" がカテゴリで、"Software" と "Hardware" がサブカテゴリである階層を設定できます。</span><span class="sxs-lookup"><span data-stu-id="054d5-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="054d5-134">この分類は、ビューアー アプリケーションによって、より整理された方法でメッセージを表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="054d5-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="054d5-135">コメント **、\*\*\*\*所有者、および\*\*\*\*番号** のエントリは、クライアント アプリケーションのユーザー インターフェイスに表示されるコメント文字列です。</span><span class="sxs-lookup"><span data-stu-id="054d5-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="054d5-136">これらは、フォーム開発者の裁量で使用できるフォーム固有のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="054d5-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="054d5-137">たとえば、コメントエントリを使用して、フォームの目的、フォームの管理を担当する人物または組織を示すために使用される所有者エントリ、およびフォームの異なるバージョンを追跡するために使用される番号を示します。</span><span class="sxs-lookup"><span data-stu-id="054d5-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="054d5-138">コメント エントリ **には** 、最大 10 行のコメントを含めできます。</span><span class="sxs-lookup"><span data-stu-id="054d5-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="054d5-139">コメントの最初の行では、キーとして "Comment" という単語を使用し、2 行目のコメントでは "Comment1" をキーとして使用し、"Comment9" を使用します。</span><span class="sxs-lookup"><span data-stu-id="054d5-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="054d5-140">**LargeIcon** および **SmallIcon** エントリは、クライアント アプリケーションのユーザー インターフェイスにアイコンを表示するために使用されるアイコン リソースのパスを指定するために使用されます。通常、これは PR_ICON ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティ列または PR_MINI_ICON (  [PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティ列を含むテーブル行の場合です。 </span><span class="sxs-lookup"><span data-stu-id="054d5-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="054d5-141">アイコン ファイル名は、フォーム構成ファイルがインストールされているディレクトリを基準にパス名として指定できます。</span><span class="sxs-lookup"><span data-stu-id="054d5-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="054d5-142">Version **エントリ** は、フォームのバージョン番号を示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="054d5-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="054d5-143">**Locale** は、移動先フォーム ライブラリの 3 文字の言語識別子です。</span><span class="sxs-lookup"><span data-stu-id="054d5-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="054d5-144">これらの識別子の一覧は  _、「Win32 プログラマリファレンス」を参照してください_。</span><span class="sxs-lookup"><span data-stu-id="054d5-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="054d5-145">[ **非表示** ] エントリは、フォームをフォーム ライブラリ プロバイダーのユーザー インターフェイスに表示するかどうかを示します。1 はファイルが非表示で、0 はフォームが表示されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="054d5-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="054d5-146">フォーム構成ファイルの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="054d5-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="054d5-147">**ComposeInFolder** エントリは、ユーザーがメッセージを作成中に保存するときに、フォームを現在のフォルダーまたはユーザーの受信トレイに配置するように設計されているかどうかを制御します。1 は、フォームが現在のフォルダーに移動することを示し、0 は受信トレイに移動することを示します。</span><span class="sxs-lookup"><span data-stu-id="054d5-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="054d5-148">**ComposeCommand** エントリは、クライアント アプリケーションの作成メニューに配置される文字列です。</span><span class="sxs-lookup"><span data-stu-id="054d5-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="054d5-149">これを指定しない場合は **、DisplayName** エントリが使用されます。</span><span class="sxs-lookup"><span data-stu-id="054d5-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


