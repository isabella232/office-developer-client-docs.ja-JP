---
title: CreateParameter メソッド (ADO)
TOCTitle: CreateParameter method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d3b36d04345df4c1d556d0607c70b3425f0047e6
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949958"
---
# <a name="createparameter-method-ado"></a><span data-ttu-id="3c833-102">CreateParameter メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="3c833-102">CreateParameter method (ADO)</span></span>

<span data-ttu-id="3c833-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3c833-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c833-104">指定したプロパティを使用して、新規 [Parameter](parameter-object-ado.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c833-104">Creates a new [Parameter](parameter-object-ado.md) object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c833-105">構文</span><span class="sxs-lookup"><span data-stu-id="3c833-105">Syntax</span></span>

<span data-ttu-id="3c833-106">**設定\*\*\*パラメーター* = *コマンド*です。CreateParameter (*名前*、*種類*、*方向*、*サイズ*、*値\*)</span><span class="sxs-lookup"><span data-stu-id="3c833-106">**Set** *parameter* = *command*.CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)</span></span>

## <a name="return-value"></a><span data-ttu-id="3c833-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="3c833-107">Return value</span></span>

<span data-ttu-id="3c833-108">**Parameter** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="3c833-108">Returns a **Parameter** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c833-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3c833-109">Parameters</span></span>

|<span data-ttu-id="3c833-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3c833-110">Parameter</span></span>|<span data-ttu-id="3c833-111">説明</span><span class="sxs-lookup"><span data-stu-id="3c833-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3c833-112">*Name*</span><span class="sxs-lookup"><span data-stu-id="3c833-112">*Name*</span></span> |<span data-ttu-id="3c833-p101">省略可能です。 **Parameter** オブジェクト名を含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c833-p101">Optional. A **String** value that contains the name of the **Parameter** object.</span></span>|
|<span data-ttu-id="3c833-115">*Type*</span><span class="sxs-lookup"><span data-stu-id="3c833-115">*Type*</span></span> |<span data-ttu-id="3c833-p102">省略可能です。 [Parameter](datatypeenum.md) オブジェクトのデータ型を **DataTypeEnum** 値で指定します。</span><span class="sxs-lookup"><span data-stu-id="3c833-p102">Optional. A [DataTypeEnum](datatypeenum.md) value that specifies the data type of the **Parameter** object.</span></span>|
|<span data-ttu-id="3c833-118">*Direction*</span><span class="sxs-lookup"><span data-stu-id="3c833-118">*Direction*</span></span> |<span data-ttu-id="3c833-p103">省略可能です。 [Parameter](parameterdirectionenum.md) オブジェクトのデータ型を **ParameterDirectionEnum** 値で指定します。</span><span class="sxs-lookup"><span data-stu-id="3c833-p103">Optional. A [ParameterDirectionEnum](parameterdirectionenum.md) value that specifies the type of **Parameter** object.</span></span>|
|<span data-ttu-id="3c833-121">*Size*</span><span class="sxs-lookup"><span data-stu-id="3c833-121">*Size*</span></span> |<span data-ttu-id="3c833-p104">省略可能です。パラメーター値の最大長を文字数またはバイト数で指定する長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c833-p104">Optional. A **Long** value that specifies the maximum length for the parameter value in characters or bytes.</span></span>|
|<span data-ttu-id="3c833-124">*Value*</span><span class="sxs-lookup"><span data-stu-id="3c833-124">*Value*</span></span> |<span data-ttu-id="3c833-p105">省略可能です。 **Parameter** オブジェクトの値を指定するバリアント型 ( **Variant** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c833-p105">Optional. A **Variant** that specifies the value for the **Parameter** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3c833-127">解説</span><span class="sxs-lookup"><span data-stu-id="3c833-127">Remarks</span></span>

<span data-ttu-id="3c833-p106">**CreateParameter** メソッドを使用して、名前、種類、方向、サイズ、および値を指定して新規 **Parameter** オブジェクトを作成します。引数に指定した値は、対応する **Parameter** プロパティに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="3c833-p106">Use the **CreateParameter** method to create a new **Parameter** object with a specified name, type, direction, size, and value. Any values you pass in the arguments are written to the corresponding **Parameter** properties.</span></span>

<span data-ttu-id="3c833-p107">このメソッドを実行しても、Parameter オブジェクトは、Command オブジェクトの Parameters コレクションに自動的に追加されません。このため、追加のプロパティを設定することができます。Parameter オブジェクトを Parameters コレクションに追加するときに、プロパティ値の妥当性が確認されます。</span><span class="sxs-lookup"><span data-stu-id="3c833-p107">This method does not automatically append the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object. This lets you set additional properties whose values ADO will validate when you append the **Parameter** object to the collection.</span></span>

<span data-ttu-id="3c833-132">*型*引数で可変長データ型を指定する場合は、*サイズ*の引数を渡すか、**パラメーター**コレクションに追加する前に**Parameter**オブジェクトの[Size](size-property-ado.md)プロパティを設定それ以外の場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="3c833-132">If you specify a variable-length data type in the *Type* argument, you must either pass a *Size* argument or set the [Size](size-property-ado.md) property of the **Parameter** object before appending it to the **Parameters** collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="3c833-133">*Type* 引数に数値型 (**adNumeric** または **adDecimal**) を指定する場合は、同時に [NumericScale](numericscale-property-ado.md) プロパティと [Precision](precision-property-ado.md) プロパティも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c833-133">If you specify a numeric data type (**adNumeric** or **adDecimal**) in the *Type* argument, then you must also set the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties.</span></span>

