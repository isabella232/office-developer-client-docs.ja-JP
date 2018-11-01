---
title: Recordset.BatchCollisions プロパティ (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4818ff1ceda746a0acb72a47e87eda58f87b2dfc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882603"
---
# <a name="recordsetbatchcollisions-property-dao"></a><span data-ttu-id="7027c-102">Recordset.BatchCollisions プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="7027c-102">Recordset.BatchCollisions Property (DAO)</span></span>


<span data-ttu-id="7027c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7027c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="7027c-104">構文</span><span class="sxs-lookup"><span data-stu-id="7027c-104">Syntax</span></span>

<span data-ttu-id="7027c-105">*式*です。BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="7027c-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="7027c-106">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="7027c-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7027c-107">注釈</span><span class="sxs-lookup"><span data-stu-id="7027c-107">Remarks</span></span>

<span data-ttu-id="7027c-p101">このプロパティには、最後に実行を試みられたバッチ **[Update](recordset-update-method-dao.md)** の呼び出し中に競合が発生した行へのブックマークの配列が含まれます。 **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** プロパティは、配列の要素の数を示します。</span><span class="sxs-lookup"><span data-stu-id="7027c-p101">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset-update-method-dao.md)** call. The **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="7027c-110">作業中の **[Recordset](recordset-object-dao.md)** オブジェクトの **[Bookmark](recordset-bookmark-property-dao.md)** プロパティを、 **BatchCollisions** 配列のブックマークの値に設定すると、最新のバッチモードの Update 操作の完了に失敗した各レコードに移動できます。</span><span class="sxs-lookup"><span data-stu-id="7027c-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="7027c-p102">競合するレコードを修正した後、バッチモードの **Update** メソッドを再び呼び出すことができます。ここで DAO はもう一度バッチ更新を試み、再び **BatchCollisions** プロパティに、2 回目の実行で失敗したレコードのセットが反映されます。以前の実行が正常に終了したレコードは、 **[RecordStatus](recordset-recordstatus-property-dao.md)** プロパティが dbRecordUnmodified に設定されているため、現在の実行には送信されません。このプロセスは、競合が発生する限り続行できますが、更新を中止して結果セットを閉じることもできます。</span><span class="sxs-lookup"><span data-stu-id="7027c-p102">After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="7027c-115">この配列は、バッチモードの **Update** メソッドを実行するたびに再作成されます。</span><span class="sxs-lookup"><span data-stu-id="7027c-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>

