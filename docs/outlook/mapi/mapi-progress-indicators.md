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
# <a name="mapi-progress-indicators"></a><span data-ttu-id="60710-103">MAPI 進行状況インジケーター</span><span class="sxs-lookup"><span data-stu-id="60710-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="60710-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60710-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60710-105">クライアントに対して実行する操作の多くは、完了するまでに長い時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="60710-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="60710-106">時間のかかる操作の進行状況をクライアントに通知するために、操作の開始からその完了までの任意の時点で、操作の完了部分をグラフィカルに表示するインジケーターを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="60710-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="60710-107">進行状況インジケーターは、完了する合計操作のパーセンテージを示しています。</span><span class="sxs-lookup"><span data-stu-id="60710-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="60710-108">次のメソッドは、時間のかかる操作と進行状況インジケーターの表示をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="60710-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="60710-109">[imapifolder:: copymessages](imapifolder-copymessages.md)、 [imapifolder:: copymessages](imapifolder-copyfolder.md)、imapifolder: [:D eletemessages](imapifolder-deletemessages.md)、imapifolder:: [eletefolder](imapifolder-deletefolder.md)、imapifolder [:: emptyfolder](imapifolder-emptyfolder.md)、 [imapifolder:: setreadflags](imapifolder-setreadflags.md)。</span><span class="sxs-lookup"><span data-stu-id="60710-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="60710-110">[imapiprop:: copyprops](imapiprop-copyprops.md)および[imapiprop:: CopyTo](imapiprop-copyto.md)。</span><span class="sxs-lookup"><span data-stu-id="60710-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="60710-111">[imapisupport::D ocopyprops](imapisupport-docopyprops.md)、 [imapisupport::D ocopyto](imapisupport-docopyto.md)、 [imapisupport:: copyfolder](imapisupport-copyfolder.md)、 [imapisupport:: copymessages](imapisupport-copymessages.md)。</span><span class="sxs-lookup"><span data-stu-id="60710-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="60710-112">[IMessage::D eleteattach](imessage-deleteattach.md)。</span><span class="sxs-lookup"><span data-stu-id="60710-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="60710-113">[IABContainer:: copyentries](iabcontainer-copyentries.md)。</span><span class="sxs-lookup"><span data-stu-id="60710-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="60710-114">進行状況インジケーターを表示するために、MAPI は progress オブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="60710-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="60710-115">Progress オブジェクトは、インジケーターの範囲を確立し、表示を作成するためのメソッドを含む[imapiprogress: IUnknown](imapiprogressiunknown.md)インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="60710-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="60710-116">MAPI では、一部のクライアントと同様に、進行状況オブジェクトの実装が提供されます。</span><span class="sxs-lookup"><span data-stu-id="60710-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="60710-117">クライアントの実装 (指定されている場合) は、操作を実行するメソッドへの入力パラメーターとして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60710-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="60710-118">クライアントが progress オブジェクトへのポインターの代わりに NULL を渡す場合は、 [imapisupport::D oprogress dialog](imapisupport-doprogressdialog.md)メソッドを呼び出して MAPI の実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="60710-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60710-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="60710-119">See also</span></span>



[<span data-ttu-id="60710-120">MAPI サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="60710-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

