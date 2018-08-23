---
title: MAPI クラッシュ回復 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: fbb6d22414daf3464e80fbf1d9cf92ccb3d560e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576590"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="08c45-103">MAPI クラッシュ回復 API について</span><span class="sxs-lookup"><span data-stu-id="08c45-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="08c45-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08c45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08c45-105">MAPI クラッシュ回復 API では、個人用フォルダー ファイル (PST) またはオフライン フォルダー ファイル (OST) の状態データが整合性の取れた状態であることを確認するためのメモリの共有を確認します。</span><span class="sxs-lookup"><span data-stu-id="08c45-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="08c45-106">コンシス テント状態の場合は、 [MAPICrashRecovery](mapicrashrecovery.md)関数は、開いているの pst ファイルまたは Ost からのデータをディスクに移動し pst ファイルまたは Ost をロックしの読み取りとデータへの書き込みアクセスが許可されません。</span><span class="sxs-lookup"><span data-stu-id="08c45-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="08c45-107">これにより、プロセスが終了するまでは、整合性の取れた状態にデータが残っています。</span><span class="sxs-lookup"><span data-stu-id="08c45-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="08c45-108">ことによって、pst ファイルまたは Ost 整合性の取れた状態でプロセスが終了する前に、Microsoft Outlook 2013 および Microsoft Outlook 2010 が次のエラー メッセージを表示することを防止し、パフォーマンスの問題を回避できます。</span><span class="sxs-lookup"><span data-stu-id="08c45-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="08c45-109">**データ ファイルを閉じませんでした正しく問題の最後に使用されていた、チェックされていること。チェックの実行中に、パフォーマンスは影響を受ける可能性があります。**</span><span class="sxs-lookup"><span data-stu-id="08c45-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="08c45-110">この API には、次のものが用意されています。</span><span class="sxs-lookup"><span data-stu-id="08c45-110">This API provides the following:</span></span>
  
<span data-ttu-id="08c45-111">定数。</span><span class="sxs-lookup"><span data-stu-id="08c45-111">Constants:</span></span>
  
- [<span data-ttu-id="08c45-112">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="08c45-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="08c45-113">関数</span><span class="sxs-lookup"><span data-stu-id="08c45-113">Functions:</span></span>
  
- [<span data-ttu-id="08c45-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="08c45-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="08c45-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="08c45-115">See also</span></span>



[<span data-ttu-id="08c45-116">MAPI クラッシュ回復 API を使用する</span><span class="sxs-lookup"><span data-stu-id="08c45-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

