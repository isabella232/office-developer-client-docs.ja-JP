---
title: MAPI の進捗状況
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8fc39c6d7da0970ee15cdd9dd67bfeef0997d7d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582869"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="cc34f-103">MAPI の進捗状況</span><span class="sxs-lookup"><span data-stu-id="cc34f-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="cc34f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc34f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc34f-105">完了するのには時間がかかる多くのクライアントに対して実行する操作のことができます。</span><span class="sxs-lookup"><span data-stu-id="cc34f-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="cc34f-106">時間のかかる操作の進行状況をクライアントに通知をするには、任意の時点で、操作の開始からその終了時に視覚的に操作の完了部分を表示するインジケーターを表示できます。</span><span class="sxs-lookup"><span data-stu-id="cc34f-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="cc34f-107">進行状況のインジケーターは、合計の操作を完了するの割合を示しています。</span><span class="sxs-lookup"><span data-stu-id="cc34f-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="cc34f-108">次の方法では、時間のかかる操作と、進行状況インジケーターの表示をサポートします。</span><span class="sxs-lookup"><span data-stu-id="cc34f-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="cc34f-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)、 [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)、 [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)、 [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)、 [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)、および[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)。</span><span class="sxs-lookup"><span data-stu-id="cc34f-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="cc34f-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md)と[IMAPIProp::CopyTo](imapiprop-copyto.md)。</span><span class="sxs-lookup"><span data-stu-id="cc34f-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="cc34f-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)、 [IMAPISupport::DoCopyTo](imapisupport-docopyto.md)、 [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)、および[IMAPISupport::CopyMessages](imapisupport-copymessages.md)。</span><span class="sxs-lookup"><span data-stu-id="cc34f-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="cc34f-112">[IMessage::DeleteAttach](imessage-deleteattach.md)。</span><span class="sxs-lookup"><span data-stu-id="cc34f-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="cc34f-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md)。</span><span class="sxs-lookup"><span data-stu-id="cc34f-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="cc34f-114">進行状況のインジケーターを表示するには、MAPI は、実行中のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="cc34f-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="cc34f-115">進行中のオブジェクトの実装、 [IMAPIProgress: IUnknown](imapiprogressiunknown.md)インタ フェース、インジケーターの範囲を確立して、表示を作成するためのメソッドを含むインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="cc34f-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="cc34f-116">MAPI は、一部のクライアントと同じように進行中のオブジェクトの実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="cc34f-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="cc34f-117">いずれかが指定した場合、操作を実行するメソッドに入力パラメーターとして、クライアントの実装を使用してください。</span><span class="sxs-lookup"><span data-stu-id="cc34f-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="cc34f-118">クライアント実行中のオブジェクトへのポインターではなく NULL が成功した場合は、 [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出すことによって MAPI の実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="cc34f-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc34f-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="cc34f-119">See also</span></span>



[<span data-ttu-id="cc34f-120">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cc34f-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

