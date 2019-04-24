---
title: フォームアイコンの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337045"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="9f296-103">フォームアイコンの表示</span><span class="sxs-lookup"><span data-stu-id="9f296-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="9f296-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f296-105">フォルダー内のメッセージの一覧を表示する場合、メッセージを標準の IPM のカスタムメッセージクラスと区別すると、ユーザーにとって便利です。メッセージを確認します。</span><span class="sxs-lookup"><span data-stu-id="9f296-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="9f296-106">カスタムメッセージクラスはフォームサーバーに対応しており、フォームサーバーはそれ自体を表すアイコンを提供します。</span><span class="sxs-lookup"><span data-stu-id="9f296-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="9f296-107">これらのアイコンをメッセージ一覧に表示して、ユーザーがメッセージを開く前に各メッセージのメッセージクラスに通知することができます。</span><span class="sxs-lookup"><span data-stu-id="9f296-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="9f296-108">通常、フォームの**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティのアイコンは、メッセージ一覧に表示される必要のあるものです。</span><span class="sxs-lookup"><span data-stu-id="9f296-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="9f296-109">フォームには、プロパティシートでフォームが最小化されているときに表示できる**PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティもあります。</span><span class="sxs-lookup"><span data-stu-id="9f296-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="9f296-110">**そのメッセージクラスのフォームサーバーをアクティブ化せずに、メッセージクラスのアイコンを取得するには**</span><span class="sxs-lookup"><span data-stu-id="9f296-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="9f296-111">[imapiformmgr:: openformcontainer](imapiformmgr-openformcontainer.md)メソッドを呼び出して、 [imapiformmgr: IUnknown](imapiformcontaineriunknown.md)インターフェイスへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="9f296-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="9f296-112">imapiformcontainer [:: ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)メソッドを呼び出して、imapiformcontainer [: imapiprop](imapiforminfoimapiprop.md)インターフェイスへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="9f296-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="9f296-113">[imapiforminfo:: makeiconfrombinary](imapiforminfo-makeiconfrombinary.md)メソッドを呼び出して、アイコンハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="9f296-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="9f296-114">このアイコンは、標準の Win32 api を使用して表示できます。</span><span class="sxs-lookup"><span data-stu-id="9f296-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9f296-115">メッセージクラスのアイコンを取得したら、そのアイコンをキャッシュするためにすべての作業を行います。</span><span class="sxs-lookup"><span data-stu-id="9f296-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="9f296-116">キャッシュされていないアイコンは、クライアントアプリケーションのパフォーマンスに重大な影響を及ぼします。</span><span class="sxs-lookup"><span data-stu-id="9f296-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="9f296-117">アイコンをキャッシュするときは、メッセージクラスとそのサブクラスの関係に注意してください。</span><span class="sxs-lookup"><span data-stu-id="9f296-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="9f296-118">たとえば、IPM.注: 取り消しメッセージクラスが発生して、IPM に再度解決します。注: IPM のすべてのサブクラスが想定されているわけではありません。注: IPM のアイコンを使用する必要があります。こと.</span><span class="sxs-lookup"><span data-stu-id="9f296-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

