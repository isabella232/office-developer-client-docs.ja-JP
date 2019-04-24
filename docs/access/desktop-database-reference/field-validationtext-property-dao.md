---
title: "\"ValidationText/エラー時\" プロパティ (DAO)"
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47bd400469bc17ac2b57bb249198f7609d7d0801
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292931"
---
# <a name="fieldvalidationtext-property-dao"></a><span data-ttu-id="fe4ab-102">"ValidationText/エラー時" プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="fe4ab-102">Field.ValidationText property (DAO)</span></span>


<span data-ttu-id="fe4ab-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe4ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe4ab-p101">**Field** オブジェクトの値が **ValidationRule** プロパティに設定されている入力規則を満たさない場合に、アプリケーションに表示するメッセージのテキストを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。  </span><span class="sxs-lookup"><span data-stu-id="fe4ab-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4ab-106">構文</span><span class="sxs-lookup"><span data-stu-id="fe4ab-106">Syntax</span></span>

<span data-ttu-id="fe4ab-107">*式*。ValidationText</span><span class="sxs-lookup"><span data-stu-id="fe4ab-107">*expression* .ValidationText</span></span>

<span data-ttu-id="fe4ab-108">\*式\***Field**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="fe4ab-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe4ab-109">注釈</span><span class="sxs-lookup"><span data-stu-id="fe4ab-109">Remarks</span></span>

<span data-ttu-id="fe4ab-p102">設定値または戻り値は、ユーザーがフィールドに無効な値を入力した場合に表示するテキストを指定する文字列型 ( **String**) の値です。コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="fe4ab-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="fe4ab-112">**Field** オブジェクトの場合、**ValidationText** プロパティの使用方法は、次の表に示すように、**Field** オブジェクトの追加先の **[Fields](fields-collection-dao.md)** コレクションを含むオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="fe4ab-112">For a **Field** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe4ab-113">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="fe4ab-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="fe4ab-114">使用方法</span><span class="sxs-lookup"><span data-stu-id="fe4ab-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe4ab-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="fe4ab-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="fe4ab-116">サポートされていません</span><span class="sxs-lookup"><span data-stu-id="fe4ab-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe4ab-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="fe4ab-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="fe4ab-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="fe4ab-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe4ab-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="fe4ab-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="fe4ab-120">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="fe4ab-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe4ab-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="fe4ab-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="fe4ab-122">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="fe4ab-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe4ab-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="fe4ab-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="fe4ab-124">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="fe4ab-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

