---
title: Recordset2.UpdateOptions プロパティ (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 508727437506e418fa2c8804cc9974f6d3ee7691
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477070"
---
# <a name="recordset2updateoptions-property-dao"></a><span data-ttu-id="14efb-102">Recordset2.UpdateOptions プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="14efb-102">Recordset2.UpdateOptions Property (DAO)</span></span>


<span data-ttu-id="14efb-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="14efb-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="14efb-104">構文</span><span class="sxs-lookup"><span data-stu-id="14efb-104">Syntax</span></span>

<span data-ttu-id="14efb-105">*式*です。UpdateOptions</span><span class="sxs-lookup"><span data-stu-id="14efb-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="14efb-106">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="14efb-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="14efb-107">注釈</span><span class="sxs-lookup"><span data-stu-id="14efb-107">Remarks</span></span>

<span data-ttu-id="14efb-108">バッチモードの **[Update](recordset2-update-method-dao.md)** を実行すると、DAO とクライアント バッチ カーソル ライブラリによって必要な変更を行う一連の SQL UPDATE ステートメントが作成されます。</span><span class="sxs-lookup"><span data-stu-id="14efb-108">When a batch-mode **[Update](recordset2-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="14efb-109">更新ごとに、 **[RecordStatus](recordset2-recordstatus-property-dao.md)** プロパティによって変更済みのマークが付けられたレコードを分離する SQL WHERE 句が作成されます。</span><span class="sxs-lookup"><span data-stu-id="14efb-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset2-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="14efb-110">一部のリモート サーバーではトリガーやその他の方法を使用して参照整合性を強制しているため、多くの場合、更新対象のフィールドを変更の影響を受けるフィールドのみに制限することが重要です。</span><span class="sxs-lookup"><span data-stu-id="14efb-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="14efb-111">そのためには、 **UpdateOptions** プロパティを **dbCriteriaKey**、 **dbCriteriaModValues**、 **dbCriteriaAllCols**、 **dbCriteriaTimeStamp** のいずれかの定数に設定します。</span><span class="sxs-lookup"><span data-stu-id="14efb-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="14efb-112">こうすると、必要最低限のトリガー コードが実行されます。</span><span class="sxs-lookup"><span data-stu-id="14efb-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="14efb-113">結果として、更新操作が速くなり、エラーの可能性も少なくなります。</span><span class="sxs-lookup"><span data-stu-id="14efb-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="14efb-p103">また、 **dbCriteriaDeleteInsert** 定数または **dbCriteriaUpdate** 定数を連結すると、バッチ変更をサーバーに返信する際に、各更新に対して SQL DELETE ステートメントと INSERT ステートメントのセット、または SQL UPDATE ステートメントを使用するかどうかを指定できます。前者の場合、レコードの更新には、2 つの異なる操作が必要となります。正しい **UpdateOptions** プロパティの設定を選択すると、パフォーマンスを大幅に向上させることができる場合があります (特にリモート システムに DELETE、INSERT、および UPDATE の各トリガーが実装されている場合)。</span><span class="sxs-lookup"><span data-stu-id="14efb-p103">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server. In the former case, two separate operations are required to update the record. In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="14efb-117">定数を指定しない場合、 **dbCriteriaUpdate** および **dbCriteriaKey** が使用されます。</span><span class="sxs-lookup"><span data-stu-id="14efb-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="14efb-118">新規レコードの追加では常に INSERT ステートメントが生成され、レコードの削除では常に DELETE ステートメントが生成されるため、このプロパティは、カーソル ライブラリによる変更レコードの更新方法にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="14efb-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

