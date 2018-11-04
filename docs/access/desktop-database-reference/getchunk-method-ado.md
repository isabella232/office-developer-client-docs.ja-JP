---
title: GetChunk メソッド (ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 27d6f2c9884441042d67615072738c7762f4f789
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949916"
---
# <a name="getchunk-method-ado"></a><span data-ttu-id="7b431-102">GetChunk メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="7b431-102">GetChunk method (ADO)</span></span>

<span data-ttu-id="7b431-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7b431-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b431-104">サイズの大きいテキスト データやバイナリ データの [Field](field-object-ado.md) オブジェクトから、内容の全体または一部を返します。</span><span class="sxs-lookup"><span data-stu-id="7b431-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b431-105">構文</span><span class="sxs-lookup"><span data-stu-id="7b431-105">Syntax</span></span>

<span data-ttu-id="7b431-106">*変数* = *フィールド*です。GetChunk (*サイズ*)</span><span class="sxs-lookup"><span data-stu-id="7b431-106">*variable* = *field*.GetChunk(*Size* )</span></span>

## <a name="return-value"></a><span data-ttu-id="7b431-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b431-107">Return value</span></span>

<span data-ttu-id="7b431-108">バリアント型 ( **Variant** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="7b431-108">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b431-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b431-109">Parameters</span></span>

|<span data-ttu-id="7b431-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b431-110">Parameter</span></span>|<span data-ttu-id="7b431-111">説明</span><span class="sxs-lookup"><span data-stu-id="7b431-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7b431-112">*Size*</span><span class="sxs-lookup"><span data-stu-id="7b431-112">*Size*</span></span> |<span data-ttu-id="7b431-113">取得するバイト数または文字数と等しい長整数型 ( **Long** ) の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="7b431-113">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7b431-114">解説</span><span class="sxs-lookup"><span data-stu-id="7b431-114">Remarks</span></span>

<span data-ttu-id="7b431-p101">**Field** オブジェクトで **GetChunk** メソッドを使用すると、オブジェクトから長いバイナリ データや文字データの一部または全体を取得できます。システム メモリに制限がある場合、 **GetChunk** メソッドを使用すると、長い値をセグメントに分けて操作できます。</span><span class="sxs-lookup"><span data-stu-id="7b431-p101">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data. In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="7b431-p102">**GetChunk** への呼び出しによって返される値は、*variable* に格納されます。*Size* が残りのデータよりも大きい場合、**GetChunk** メソッドは、*variable* の余った部分を空白で埋めることはなく、残りのデータのみを返します。フィールドが空の場合、**GetChunk** メソッドは Null 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7b431-p102">The data that a **GetChunk** call returns is assigned to *variable*. If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces. If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="7b431-p103">**GetChunk** を連続して呼び出すと、直前の **GetChunk** の呼び出しで取得されたデータの直後からデータが取得されます。ただし、あるフィールドのデータを取得しているときに、カレント レコードの別のフィールド値の設定または読み取りを行うと、最初のフィールドからのデータ取得は終了したと見なされます。最初のフィールドでもう一度 **GetChunk** メソッドを呼び出すと、新規の **GetChunk** 操作と解釈され、データ先頭から読み取りが開始されます。最初の [Recordset](recordset-object-ado.md) オブジェクトの複製を除く別の **Recordset** オブジェクトのフィールドにアクセスした場合、 **GetChunk** の操作は中断されません。</span><span class="sxs-lookup"><span data-stu-id="7b431-p103">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off. However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field. If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="7b431-124">**Field** オブジェクトの [Attributes](attributes-property-ado.md) プロパティで **adFldLong** ビットが **True** に設定されていると、そのフィールドで **GetChunk** メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b431-124">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="7b431-125">**Field** オブジェクトで **GetChunk** メソッドを使用する際にカレント レコードがないと、エラー 3021 (カレント レコードがありません) が発生します。</span><span class="sxs-lookup"><span data-stu-id="7b431-125">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="7b431-p104">[!メモ] **GetChunk** メソッドでは、 **Record** オブジェクトの [Field](record-object-ado.md) オブジェクトを操作できません。操作は何も実行されず、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7b431-p104">The **GetChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object. It does not perform any operation and will produce a run-time error.</span></span>


