---
title: MAPI クラッシュ回復 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420263"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="29be1-103">MAPI クラッシュ回復 API について</span><span class="sxs-lookup"><span data-stu-id="29be1-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="29be1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29be1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29be1-105">MAPI クラッシュ回復 API は、個人用フォルダーファイル (PST) またはオフラインフォルダーファイル (OST) の共有メモリの状態をチェックして、データが一貫性のある状態であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="29be1-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="29be1-106">整合状態にある場合、 [mapicrashrecovery](mapicrashrecovery.md)関数は、open pst または ost からディスクにデータを移動し、pst または ost をロックし、データへの読み取りまたは書き込みアクセスを許可しません。</span><span class="sxs-lookup"><span data-stu-id="29be1-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="29be1-107">これにより、プロセスが終了するまで、データは一貫した状態に保たれます。</span><span class="sxs-lookup"><span data-stu-id="29be1-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="29be1-108">プロセスが終了する前に、pst または ost が一貫した状態になっていることを確認することにより、microsoft outlook 2013 と microsoft outlook 2010 が次のエラーメッセージを表示しないようにして、パフォーマンスの問題を回避することができます。</span><span class="sxs-lookup"><span data-stu-id="29be1-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="29be1-109">**データファイルが前回使用され、問題がないかチェックされているときに、データファイルが正常に閉じられませんでした。チェックが進行している間は、パフォーマンスが影響を受ける可能性があります。**</span><span class="sxs-lookup"><span data-stu-id="29be1-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="29be1-110">この API は、次の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="29be1-110">This API provides the following:</span></span>
  
<span data-ttu-id="29be1-111">定数</span><span class="sxs-lookup"><span data-stu-id="29be1-111">Constants:</span></span>
  
- [<span data-ttu-id="29be1-112">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="29be1-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="29be1-113">関数</span><span class="sxs-lookup"><span data-stu-id="29be1-113">Functions:</span></span>
  
- [<span data-ttu-id="29be1-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="29be1-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="29be1-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="29be1-115">See also</span></span>



[<span data-ttu-id="29be1-116">MAPI クラッシュ回復 API を使用する</span><span class="sxs-lookup"><span data-stu-id="29be1-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

