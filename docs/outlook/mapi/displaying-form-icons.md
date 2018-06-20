---
title: フォームのアイコンを表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b2e79e5568de38bee9a97c9df2598b30f1ba1bdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799940"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="9622c-103">フォームのアイコンを表示します。</span><span class="sxs-lookup"><span data-stu-id="9622c-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="9622c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9622c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9622c-105">、フォルダー内のメッセージの一覧を表示するとき、ユーザーに役に立つ場合は標準の IPM とカスタム メッセージ クラスを持つメッセージを区別します。メッセージに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9622c-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="9622c-106">カスタム メッセージ クラスは、フォームのサーバーに対応し、フォーム サーバーが自身を表すアイコンを提供します。</span><span class="sxs-lookup"><span data-stu-id="9622c-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="9622c-107">ユーザーがメッセージを開く前に、各メッセージのメッセージ クラスにユーザーに警告するメッセージの一覧にこれらのアイコンを表示できます。</span><span class="sxs-lookup"><span data-stu-id="9622c-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="9622c-108">通常、フォームの**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) のプロパティのアイコンは、メッセージの一覧に表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9622c-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="9622c-109">フォームには、プロパティ シートでフォームが最小化したときに表示できる**PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティが設定されています。</span><span class="sxs-lookup"><span data-stu-id="9622c-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="9622c-110">**そのメッセージ クラスのフォームのサーバーをアクティブにすることがなく、メッセージ クラスのアイコンを取得するには**</span><span class="sxs-lookup"><span data-stu-id="9622c-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="9622c-111">ポインターを取得する[IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md)メソッドを呼び出して、 [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="9622c-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="9622c-112">ポインターを取得する[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)メソッドを呼び出して、 [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="9622c-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="9622c-113">アイコンのハンドルを取得する[IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9622c-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="9622c-114">標準の Win32 Api を使用してアイコンを表示し、ことができます。</span><span class="sxs-lookup"><span data-stu-id="9622c-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9622c-115">メッセージ クラスのアイコンがある場合は、そのアイコンをキャッシュするよう努力することです。</span><span class="sxs-lookup"><span data-stu-id="9622c-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="9622c-116">クライアント アプリケーションのパフォーマンスに影響を与える深刻なアイコンをキャッシュしません。</span><span class="sxs-lookup"><span data-stu-id="9622c-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="9622c-117">アイコンをキャッシュする場合は、メッセージ クラスとそのサブクラスの関係の注意します。</span><span class="sxs-lookup"><span data-stu-id="9622c-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="9622c-118">などの場合は、IPM。Note.Meeting.Cancel メッセージ クラスは IPM に解決するために発生します。注意してくださいと仮定しないでをすべて IPM のサブクラスです。注記では、IPM のアイコンを使用する必要があります。注意してください。</span><span class="sxs-lookup"><span data-stu-id="9622c-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

