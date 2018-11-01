---
title: Field2.ValidationText プロパティ (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b8ce99f7fbedc487f5c5bae98745f1d446c2da3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867147"
---
# <a name="field2validationtext-property-dao"></a><span data-ttu-id="90ad7-102">Field2.ValidationText プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="90ad7-102">Field2.ValidationText Property (DAO)</span></span>


<span data-ttu-id="90ad7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="90ad7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90ad7-p101">**Field2** オブジェクトの値が **ValidationRule** プロパティに設定されている入力規則を満たさない場合に、アプリケーションに表示するメッセージのテキストを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="90ad7-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field2** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ad7-106">構文</span><span class="sxs-lookup"><span data-stu-id="90ad7-106">Syntax</span></span>

<span data-ttu-id="90ad7-107">*式*です。ValidationText</span><span class="sxs-lookup"><span data-stu-id="90ad7-107">*expression* .ValidationText</span></span>

<span data-ttu-id="90ad7-108">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="90ad7-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ad7-109">注釈</span><span class="sxs-lookup"><span data-stu-id="90ad7-109">Remarks</span></span>

<span data-ttu-id="90ad7-p102">設定値または戻り値は、ユーザーがフィールドに無効な値を入力した場合に表示するテキストを指定する文字列型 ( **String**) の値です。コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="90ad7-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="90ad7-112">**Field2** では、 **ValidationText** プロパティの使用方法は、次の表に示すように、 [Field2](fields-collection-dao.md) オブジェクトを追加する \*\*\*\*Fields\*\*\*\* コレクションが含まれているオブジェクトに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="90ad7-112">For a **Field2** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field2** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90ad7-113">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="90ad7-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="90ad7-114">使用例</span><span class="sxs-lookup"><span data-stu-id="90ad7-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90ad7-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="90ad7-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="90ad7-116">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="90ad7-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90ad7-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="90ad7-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="90ad7-118">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="90ad7-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90ad7-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="90ad7-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="90ad7-120">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="90ad7-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90ad7-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="90ad7-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="90ad7-122">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="90ad7-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90ad7-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="90ad7-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="90ad7-124">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="90ad7-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

