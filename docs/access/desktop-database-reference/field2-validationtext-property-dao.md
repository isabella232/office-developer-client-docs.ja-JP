---
title: Field2.ValidationText プロパティ (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d971b14093dd02204327e6f0ef30a81c6567c5bc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479441"
---
# <a name="field2validationtext-property-dao"></a><span data-ttu-id="d3cec-102">Field2.ValidationText プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="d3cec-102">Field2.ValidationText Property (DAO)</span></span>


<span data-ttu-id="d3cec-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3cec-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d3cec-p101">**Field2** オブジェクトの値が **ValidationRule** プロパティに設定されている入力規則を満たさない場合に、アプリケーションに表示するメッセージのテキストを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d3cec-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field2** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3cec-106">構文</span><span class="sxs-lookup"><span data-stu-id="d3cec-106">Syntax</span></span>

<span data-ttu-id="d3cec-107">*式*です。ValidationText</span><span class="sxs-lookup"><span data-stu-id="d3cec-107">*expression* .ValidationText</span></span>

<span data-ttu-id="d3cec-108">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="d3cec-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3cec-109">注釈</span><span class="sxs-lookup"><span data-stu-id="d3cec-109">Remarks</span></span>

<span data-ttu-id="d3cec-p102">設定値または戻り値は、ユーザーがフィールドに無効な値を入力した場合に表示するテキストを指定する文字列型 ( **String**) の値です。コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="d3cec-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="d3cec-112">**Field2** では、 **ValidationText** プロパティの使用方法は、次の表に示すように、 [Field2](fields-collection-dao.md) オブジェクトを追加する \*\*\*\*Fields\*\*\*\* コレクションが含まれているオブジェクトに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="d3cec-112">For a **Field2** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field2** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d3cec-113">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="d3cec-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="d3cec-114">使用例</span><span class="sxs-lookup"><span data-stu-id="d3cec-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3cec-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="d3cec-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="d3cec-116">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="d3cec-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3cec-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="d3cec-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d3cec-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="d3cec-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3cec-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="d3cec-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="d3cec-120">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="d3cec-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3cec-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="d3cec-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="d3cec-122">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="d3cec-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3cec-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="d3cec-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="d3cec-124">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="d3cec-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

