---
title: originalvalue プロパティ (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288183"
---
# <a name="originalvalue-property-ado"></a><span data-ttu-id="a3925-102">originalvalue プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="a3925-102">OriginalValue property (ADO)</span></span>

<span data-ttu-id="a3925-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3925-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3925-104">変更が行われる前のレコードに存在していた [Field](field-object-ado.md) の値を示します。</span><span class="sxs-lookup"><span data-stu-id="a3925-104">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3925-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="a3925-105">Return value</span></span>

<span data-ttu-id="a3925-106">変更前のフィールドの値を表すバリアント型 (**Variant**) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="a3925-106">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3925-107">注釈</span><span class="sxs-lookup"><span data-stu-id="a3925-107">Remarks</span></span>

<span data-ttu-id="a3925-108">現在のレコードからフィールドの元の値を返すには、**OriginalValue** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a3925-108">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="a3925-109">*即時更新モード*(プロバイダーが[update](update-method-ado.md)メソッドを呼び出した後に、基になるデータソースに変更を書き込む) では、 **originalvalue**プロパティは、変更の前に存在したフィールド値を返します (つまり、last **Update**メソッドの呼び出し)。</span><span class="sxs-lookup"><span data-stu-id="a3925-109">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="a3925-110">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span><span class="sxs-lookup"><span data-stu-id="a3925-110">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="a3925-111">*バッチ更新モード*(プロバイダーが複数の変更をキャッシュし、 [UpdateBatch](updatebatch-method-ado.md)メソッドを呼び出したときに、基になるデータソースにそれらを書き込みます) では、 **originalvalue**プロパティは、いずれかの前にあったフィールド値を返します。変更 (前回の**UpdateBatch**メソッドの呼び出し以降)。</span><span class="sxs-lookup"><span data-stu-id="a3925-111">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call).</span></span> <span data-ttu-id="a3925-112">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span><span class="sxs-lookup"><span data-stu-id="a3925-112">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span></span> <span data-ttu-id="a3925-113">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span><span class="sxs-lookup"><span data-stu-id="a3925-113">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="a3925-114">Record</span><span class="sxs-lookup"><span data-stu-id="a3925-114">Record</span></span>

<span data-ttu-id="a3925-115">[Record](record-object-ado.md) オブジェクトの場合、[Update](update-method-ado.md) を呼び出す前に追加されたフィールドの **OriginalValue** プロパティは空になります。</span><span class="sxs-lookup"><span data-stu-id="a3925-115">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

