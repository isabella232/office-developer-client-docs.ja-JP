---
title: フォーム アイコンの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438632"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="ce81e-103">フォーム アイコンの表示</span><span class="sxs-lookup"><span data-stu-id="ce81e-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="ce81e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce81e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce81e-105">フォルダーにメッセージの一覧を表示する場合、カスタム メッセージ クラスを持つメッセージと標準 IPM を区別する場合は、ユーザーに役立ちます。メモ メッセージ。</span><span class="sxs-lookup"><span data-stu-id="ce81e-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="ce81e-106">カスタム メッセージ クラスはフォーム サーバーに対応し、フォーム サーバーは自分自身を表すアイコンを提供します。</span><span class="sxs-lookup"><span data-stu-id="ce81e-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="ce81e-107">これらのアイコンをメッセージの一覧に表示して、ユーザーがメッセージを開く前に、各メッセージのメッセージ クラスにユーザーに通知できます。</span><span class="sxs-lookup"><span data-stu-id="ce81e-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="ce81e-108">通常、メッセージの一覧にPR_MINI_ICON **(** [PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティのアイコンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce81e-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="ce81e-109">フォームには、プロパティ **PR_ICON** でフォームを最小化するときに表示できるプロパティ [(PidTagIcon)](pidtagicon-canonical-property.md)もあります。</span><span class="sxs-lookup"><span data-stu-id="ce81e-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="ce81e-110">**そのメッセージ クラスのフォーム サーバーをアクティブ化せずにメッセージ クラスのアイコンを取得するには**</span><span class="sxs-lookup"><span data-stu-id="ce81e-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="ce81e-111">[IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md)メソッドを呼び出して[、IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)インターフェイスへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="ce81e-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="ce81e-112">[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)メソッドを呼び出して[、IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)インターフェイスへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="ce81e-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="ce81e-113">アイコン ハンドル [を取得するには、IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ce81e-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="ce81e-114">このアイコンは、標準の Win32 API を使用して表示できます。</span><span class="sxs-lookup"><span data-stu-id="ce81e-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ce81e-115">メッセージ クラスのアイコンを取得したら、そのアイコンをキャッシュするためにあらゆる努力をします。</span><span class="sxs-lookup"><span data-stu-id="ce81e-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="ce81e-116">アイコンをキャッシュしないは、クライアント アプリケーションのパフォーマンスに重大な影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="ce81e-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="ce81e-117">アイコンをキャッシュする場合は、メッセージ クラスとそのサブクラス間の関係に注意してください。</span><span class="sxs-lookup"><span data-stu-id="ce81e-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="ce81e-118">たとえば、IPM の場合です。メモ.Meeting.Cancel メッセージ クラスは IPM に解決されます。注: IPM のすべてのサブクラスを想定していない。メモでは、IPM のアイコンを使用する必要があります。注。</span><span class="sxs-lookup"><span data-stu-id="ce81e-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

