---
title: Index プロパティ (ADO)
TOCTitle: Index property (ADO)
ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15)
ms:contentKeyID: 48544715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d436ec9102c4c75688b6c6ac973ca85e8c280d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291707"
---
# <a name="index-property-ado"></a><span data-ttu-id="951d4-102">Index プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="951d4-102">Index property (ADO)</span></span>


<span data-ttu-id="951d4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="951d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="951d4-104">[Recordset](recordset-object-ado.md) オブジェクトに対して現在有効なインデックスの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="951d4-104">Indicates the name of the index currently in effect for a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="951d4-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="951d4-105">Settings and return values</span></span>

<span data-ttu-id="951d4-106">インデックス名を表す文字列型 (**String**) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="951d4-106">Sets or returns a **String** value, which is the name of the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="951d4-107">注釈</span><span class="sxs-lookup"><span data-stu-id="951d4-107">Remarks</span></span>

<span data-ttu-id="951d4-p101">**Index** プロパティで指定したインデックスは、 **Recordset** オブジェクトの基になるベース テーブルで事前に宣言しておく必要があります。つまり、インデックスは、ADOX [Index](index-object-adox.md) オブジェクトとしてプログラムで宣言しておくか、ベース テーブルの作成時に宣言しておきます。</span><span class="sxs-lookup"><span data-stu-id="951d4-p101">The index named by the **Index** property must have previously been declared on the base table underlying the **Recordset** object. That is, the index must have been declared programmatically either as an ADOX [Index](index-object-adox.md) object, or when the base table was created.</span></span>

<span data-ttu-id="951d4-p102">インデックスを設定できないと、実行時エラーが発生します。次の条件では、 **Index** プロパティを設定できません。</span><span class="sxs-lookup"><span data-stu-id="951d4-p102">A run-time error will occur if the index cannot be set. The **Index** property cannot be set:</span></span>

  - <span data-ttu-id="951d4-112">[WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) イベント ハンドラーまたは **RecordsetChangeComplete** イベント ハンドラー内。</span><span class="sxs-lookup"><span data-stu-id="951d4-112">Within a [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) or **RecordsetChangeComplete** event handler.</span></span>

  - <span data-ttu-id="951d4-113">**Recordset** の操作が実行中である ( [State](state-property-ado.md) プロパティで判別可能)。</span><span class="sxs-lookup"><span data-stu-id="951d4-113">If the **Recordset** is still executing an operation (which can be determined by the [State](state-property-ado.md) property).</span></span>

  - <span data-ttu-id="951d4-114">**Filter** プロパティにより [Recordset](filter-property-ado.md) にフィルターが設定されている。</span><span class="sxs-lookup"><span data-stu-id="951d4-114">If a filter has been set on the **Recordset** with the [Filter](filter-property-ado.md) property.</span></span>

<span data-ttu-id="951d4-115">**Recordset** が閉じていれば、 **Index** プロパティは正常に設定できますが、基になるプロバイダーがインデックスをサポートしていない場合は、 **Recordset** が正常に開かなかったり、インデックスを使うことができないことがあります。</span><span class="sxs-lookup"><span data-stu-id="951d4-115">The **Index** property can always be set successfully if the **Recordset** is closed, but the **Recordset** will not open successfully, or the index will not be usable, if the underlying provider does not support indexes.</span></span>

<span data-ttu-id="951d4-p103">インデックスを設定すると、現在の行の位置が変更されることがあります。その場合は、[AbsolutePosition](absoluteposition-property-ado.md) プロパティが更新され、 **WillChangeRecordset** イベント、 **RecordsetChangeComplete** イベント、 [WillMove](willmove-and-movecomplete-events-ado.md) イベント、および [MoveComplete](willmove-and-movecomplete-events-ado.md) イベントが生成されます。</span><span class="sxs-lookup"><span data-stu-id="951d4-p103">If the index can be set, the current row position may change. This will cause an update to the [AbsolutePosition](absoluteposition-property-ado.md) property, and the generation of **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md), and [MoveComplete](willmove-and-movecomplete-events-ado.md) events.</span></span>

<span data-ttu-id="951d4-p104">インデックスの設定が可能で、[LockType](locktype-property-ado.md) プロパティが **adLockPessimistic** または **adLockOptimistic** の場合は、 [UpdateBatch](updatebatch-method-ado.md) 操作が暗黙的に実行されます。これによって、現在のグループと、影響下のグループが解放されます。既存のフィルターがすべて解放され、現在の行の位置は、並べ替えられた **Recordset** の最初の行に移動します。</span><span class="sxs-lookup"><span data-stu-id="951d4-p104">If the index can be set and the [LockType](locktype-property-ado.md) property is **adLockPessimistic** or **adLockOptimistic**, then an implicit [UpdateBatch](updatebatch-method-ado.md) operation is performed. This releases the current and affected groups. Any existing filter is released, and the current row position is changed to the first row of the reordered **Recordset**.</span></span>

<span data-ttu-id="951d4-121">**Index** プロパティは、 [Seek](seek-method-ado.md) メソッドと一緒に使用します。</span><span class="sxs-lookup"><span data-stu-id="951d4-121">The **Index** property is used in conjunction with the [Seek](seek-method-ado.md) method.</span></span> <span data-ttu-id="951d4-122">基になるプロバイダーが **Index** プロパティをサポートしていないために **Seek** メソッドがサポートされていない場合は、代わりに [Find](find-method-ado.md) メソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="951d4-122">If the underlying provider does not support the **Index** property, and thus the **Seek** method, consider using the [Find](find-method-ado.md) method instead.</span></span> <span data-ttu-id="951d4-123">**Recordset**オブジェクトが、 [supports](supports-method-ado.md)メソッド **(adindex)** でのインデックスをサポートしているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="951d4-123">Determine whether the **Recordset** object supports indexes with the [Supports](supports-method-ado.md)**(adIndex)** method.</span></span>

<span data-ttu-id="951d4-124">どちらもインデックスを扱いますが、組み込み **Index** プロパティは、動的な [Optimize](optimize-property-dynamic-ado.md) プロパティとは無関係です。</span><span class="sxs-lookup"><span data-stu-id="951d4-124">The built-in **Index** property is not related to the dynamic [Optimize](optimize-property-dynamic-ado.md) property, although they both deal with indexes.</span></span>

