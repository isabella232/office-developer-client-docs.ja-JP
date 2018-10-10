---
title: AppendChunk メソッド (ADO)
TOCTitle: AppendChunk Method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a565430cf81eed5cbc1ebfe135ce80ee6f0177e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479103"
---
# <a name="appendchunk-method-ado"></a><span data-ttu-id="ee484-102">AppendChunk メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="ee484-102">AppendChunk Method (ADO)</span></span>


<span data-ttu-id="ee484-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee484-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="ee484-104">大きなサイズのテキストまたはバイナリ データの [Field](field-object-ado.md) オブジェクト、または [Parameter](parameter-object-ado.md) オブジェクトにデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="ee484-104">Appends data to a large text or binary data [Field](field-object-ado.md), or to a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee484-105">構文</span><span class="sxs-lookup"><span data-stu-id="ee484-105">Syntax</span></span>

<span data-ttu-id="ee484-106">*オブジェクトです*。AppendChunk*データ*</span><span class="sxs-lookup"><span data-stu-id="ee484-106">*object.* AppendChunk *Data*</span></span>

## <a name="parameters"></a><span data-ttu-id="ee484-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ee484-107">Parameters</span></span>

  - <span data-ttu-id="ee484-108">*object*</span><span class="sxs-lookup"><span data-stu-id="ee484-108">*object*</span></span>

  - <span data-ttu-id="ee484-109">**Field** オブジェクトまたは **Parameter** オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee484-109">A **Field** or **Parameter** object.</span></span>

  - <span data-ttu-id="ee484-110">*Data*</span><span class="sxs-lookup"><span data-stu-id="ee484-110">*Data*</span></span>

  - <span data-ttu-id="ee484-111">オブジェクトに追加するデータを含むバリアント型 ( **Variant** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ee484-111">A **Variant** that contains the data to append to the object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee484-112">解説</span><span class="sxs-lookup"><span data-stu-id="ee484-112">Remarks</span></span>

<span data-ttu-id="ee484-p101">**AppendChunk** メソッドは、長いバイナリ データまたは文字データを格納するために、 **Field** オブジェクトまたは **Parameter** オブジェクトに対して使用します。システムのメモリに制限がある場合は、 **AppendChunk** メソッドを使用することで、長い値を全体としてではなく、複数の部分に分けて操作できます。</span><span class="sxs-lookup"><span data-stu-id="ee484-p101">Use the **AppendChunk** method on a **Field** or **Parameter** object to fill it with long binary or character data. In situations where system memory is limited, you can use the **AppendChunk** method to manipulate long values in portions rather than in their entirety.</span></span>

<span data-ttu-id="ee484-115">**Field**</span><span class="sxs-lookup"><span data-stu-id="ee484-115">**Field**</span></span>

<span data-ttu-id="ee484-116">**Field** オブジェクトの [Attributes](attributes-property-ado.md) プロパティの **adFldLong** ビットが True に設定されている場合は、そのフィールドに対して **AppendChunk** メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee484-116">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to true, you can use the **AppendChunk** method for that field.</span></span>

<span data-ttu-id="ee484-p102">**Field** オブジェクトに対する **AppendChunk** メソッドの最初の呼び出しでフィールドにデータが書き込まれ、既存のデータが上書きされます。それ以降の **AppendChunk** の呼び出しでは、既存のデータに追加されます。あるフィールドにデータを追加し、その後、カレント レコードの別のフィールド値の設定または読み取りを行うと、最初のフィールドへのデータの追加は終了したものと見なされます。最初のフィールドに対して再度 **AppendChunk** メソッドを呼び出すと、新しい **AppendChunk** 操作と解釈され、既存のデータが上書きされます。最初の [Recordset](recordset-object-ado.md) オブジェクトの複製を除く他の **Recordset** オブジェクトのフィールドにアクセスした場合は、 **AppendChunk** 操作は中断されません。</span><span class="sxs-lookup"><span data-stu-id="ee484-p102">The first **AppendChunk** call on a **Field** object writes data to the field, overwriting any existing data. Subsequent **AppendChunk** calls add to existing data. If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field. If you call the **AppendChunk** method on the first field again, ADO interprets the call as a new **AppendChunk** operation and overwrites the existing data. Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **AppendChunk** operations.</span></span>

<span data-ttu-id="ee484-122">**Field** オブジェクトで **AppendChunk** を呼び出したときにカレント レコードが存在しないと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ee484-122">If there is no current record when you call **AppendChunk** on a **Field** object, an error occurs.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ee484-p103">[!メモ] <STRONG>AppendChunk</STRONG> メソッドでは、 <STRONG>Record</STRONG> オブジェクトの <A href="record-object-ado.md">Field</A> オブジェクトを操作できません。操作は何も実行されず、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ee484-p103">The <STRONG>AppendChunk</STRONG> method does not operate on <STRONG>Field</STRONG> objects of a <A href="record-object-ado.md">Record</A> object. It does not perform any operation and will produce a run-time error.</span></span></P>



<span data-ttu-id="ee484-125">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="ee484-125">**Parameter**</span></span>

<span data-ttu-id="ee484-126">**Parameter** オブジェクトの **Attributes** プロパティの **adParamLong** ビットが True に設定されていると、そのパラメーターに対して **AppendChunk** メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee484-126">If the **adParamLong** bit in the **Attributes** property of a **Parameter** object is set to true, you can use the **AppendChunk** method for that parameter.</span></span>

<span data-ttu-id="ee484-p104">**Parameter** オブジェクトに対する **AppendChunk** メソッドの最初の呼び出しではパラメーターにデータが書き込まれ、既存のデータが上書きされます。それ以降の **Parameter** オブジェクトに対する **AppendChunk** の呼び出しでは、既存のパラメーター データに追加されます。 **AppendChunk** メソッドの呼び出しで Null 値を渡すと、すべてのパラメーター データが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="ee484-p104">The first **AppendChunk** call on a **Parameter** object writes data to the parameter, overwriting any existing data. Subsequent **AppendChunk** calls on a **Parameter** object add to existing parameter data. An **AppendChunk** call that passes a null value discards all of the parameter data.</span></span>
