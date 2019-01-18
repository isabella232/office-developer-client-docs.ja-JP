---
title: Field2.ValidationText プロパティ (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4d58cb6bd32bd46b0a6bcec40ff68cdc52eebc31
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698247"
---
# <a name="field2validationtext-property-dao"></a><span data-ttu-id="10f3c-102">Field2.ValidationText プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="10f3c-102">Field2.ValidationText property (DAO)</span></span>


<span data-ttu-id="10f3c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="10f3c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10f3c-p101">**Field2** オブジェクトの値が **ValidationRule** プロパティに設定されている入力規則を満たさない場合に、アプリケーションに表示するメッセージのテキストを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="10f3c-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field2** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="10f3c-106">構文</span><span class="sxs-lookup"><span data-stu-id="10f3c-106">Syntax</span></span>

<span data-ttu-id="10f3c-107">*式*です。ValidationText</span><span class="sxs-lookup"><span data-stu-id="10f3c-107">*expression* .ValidationText</span></span>

<span data-ttu-id="10f3c-108">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="10f3c-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="10f3c-109">注釈</span><span class="sxs-lookup"><span data-stu-id="10f3c-109">Remarks</span></span>

<span data-ttu-id="10f3c-p102">設定値または戻り値は、ユーザーがフィールドに無効な値を入力した場合に表示するテキストを指定する文字列型 ( **String**) の値です。コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="10f3c-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="10f3c-112">**Field2** では、 **ValidationText** プロパティの使用方法は、次の表に示すように、 [Field2](fields-collection-dao.md) オブジェクトを追加する \*\*\*\*Fields\*\*\*\* コレクションが含まれているオブジェクトに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="10f3c-112">For a **Field2** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field2** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10f3c-113">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="10f3c-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="10f3c-114">使用例</span><span class="sxs-lookup"><span data-stu-id="10f3c-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10f3c-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="10f3c-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="10f3c-116">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="10f3c-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f3c-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="10f3c-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="10f3c-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="10f3c-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f3c-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="10f3c-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="10f3c-120">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="10f3c-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10f3c-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="10f3c-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="10f3c-122">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="10f3c-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10f3c-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="10f3c-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="10f3c-124">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="10f3c-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

