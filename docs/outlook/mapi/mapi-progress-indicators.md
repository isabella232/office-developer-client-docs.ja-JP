---
title: MAPI 進行状況インジケーター
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410708"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="70317-103">MAPI 進行状況インジケーター</span><span class="sxs-lookup"><span data-stu-id="70317-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="70317-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70317-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70317-105">クライアントに対して実行する操作の多くは、完了に長い時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="70317-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="70317-106">長い操作の進行状況をクライアントに通知するには、操作の開始から完了まで、任意の時点で操作の終了部分をグラフィカルに表示するインジケーターを表示できます。</span><span class="sxs-lookup"><span data-stu-id="70317-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="70317-107">進行状況インジケーターには、完了する操作全体の割合が表示されます。</span><span class="sxs-lookup"><span data-stu-id="70317-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="70317-108">次のメソッドは、長い操作と進行状況インジケーターの表示をサポートします。</span><span class="sxs-lookup"><span data-stu-id="70317-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="70317-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::D eleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="70317-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="70317-110">[IMAPIProp::CopyProps と](imapiprop-copyprops.md) [IMAPIProp::CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="70317-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="70317-111">[IMAPISupport::D oCopyProps](imapisupport-docopyprops.md), [IMAPISupport::D oCopyTo](imapisupport-docopyto.md), [IMAPISupport:::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="70317-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="70317-112">[IMessage::D eleteAttach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="70317-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="70317-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="70317-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="70317-114">進行状況インジケーターを表示するために、MAPI は進行状況オブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="70317-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="70317-115">Progress オブジェクトは [、IMAPIProgress : IUnknown](imapiprogressiunknown.md) インターフェイス、インジケーターの範囲を確立し、ディスプレイを作成するためのメソッドを含むインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="70317-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="70317-116">MAPI は、一部のクライアントと同様に進行状況オブジェクトの実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="70317-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="70317-117">クライアントの実装が指定されている場合は、操作を実行するメソッドの入力パラメーターとして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="70317-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="70317-118">クライアントが進行状況オブジェクトへのポインターではなく NULL を渡す場合は [、IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) メソッドを呼び出して MAPI の実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="70317-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70317-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="70317-119">See also</span></span>



[<span data-ttu-id="70317-120">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="70317-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

