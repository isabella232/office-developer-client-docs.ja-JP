---
title: メソッド (ADO Fields コレクション) を削除します。
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b33c15adf1d079e2da12590891d950aa35e5414f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950176"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="374ea-102">メソッド (ADO Fields コレクション) を削除します。</span><span class="sxs-lookup"><span data-stu-id="374ea-102">Delete method (ADO Fields Collection)</span></span>

<span data-ttu-id="374ea-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="374ea-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="374ea-104">[Fields](fields-collection-ado.md) コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="374ea-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="374ea-105">構文</span><span class="sxs-lookup"><span data-stu-id="374ea-105">Syntax</span></span>

<span data-ttu-id="374ea-106">*フィールド*です。*フィールド*を削除します。</span><span class="sxs-lookup"><span data-stu-id="374ea-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="374ea-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="374ea-107">Parameters</span></span>

|<span data-ttu-id="374ea-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="374ea-108">Parameter</span></span>|<span data-ttu-id="374ea-109">説明</span><span class="sxs-lookup"><span data-stu-id="374ea-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="374ea-110">*Field*</span><span class="sxs-lookup"><span data-stu-id="374ea-110">*Field*</span></span> |<span data-ttu-id="374ea-p101">削除する **Field** オブジェクトを指定するバリアント型 ( [Variant](field-object-ado.md) ) の値です。このパラメーターには、 **Field** オブジェクトの名前または **Field** オブジェクト自体のインデックスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="374ea-p101">A **Variant** that designates the [Field](field-object-ado.md) object to delete. This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>|

## <a name="remarks"></a><span data-ttu-id="374ea-113">解説</span><span class="sxs-lookup"><span data-stu-id="374ea-113">Remarks</span></span>

<span data-ttu-id="374ea-114">**Fields.Delete** メソッドを開いている [Recordset](recordset-object-ado.md) に対して呼び出すと、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="374ea-114">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

