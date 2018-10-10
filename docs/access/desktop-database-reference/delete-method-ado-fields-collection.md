---
title: Delete メソッド (ADO Fields コレクション)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3dc4d3553113a35fba875c3eb23ec544ea3d6b7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478179"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="30d0f-102">Delete メソッド (ADO Fields コレクション)</span><span class="sxs-lookup"><span data-stu-id="30d0f-102">Delete Method (ADO Fields Collection)</span></span>


<span data-ttu-id="30d0f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="30d0f-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="30d0f-104">[Fields](fields-collection-ado.md) コレクションからオブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="30d0f-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="30d0f-105">構文</span><span class="sxs-lookup"><span data-stu-id="30d0f-105">Syntax</span></span>

<span data-ttu-id="30d0f-106">*フィールド*です。*フィールド*を削除します。</span><span class="sxs-lookup"><span data-stu-id="30d0f-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="30d0f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="30d0f-107">Parameters</span></span>

  - <span data-ttu-id="30d0f-108">*Field*</span><span class="sxs-lookup"><span data-stu-id="30d0f-108">*Field*</span></span>

  - <span data-ttu-id="30d0f-p101">削除する **Field** オブジェクトを指定するバリアント型 ( [Variant](field-object-ado.md) ) の値です。このパラメーターには、 **Field** オブジェクトの名前または **Field** オブジェクト自体のインデックスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="30d0f-p101">A **Variant** that designates the [Field](field-object-ado.md) object to delete. This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>

## <a name="remarks"></a><span data-ttu-id="30d0f-111">解説</span><span class="sxs-lookup"><span data-stu-id="30d0f-111">Remarks</span></span>

<span data-ttu-id="30d0f-112">**Fields.Delete** メソッドを開いている [Recordset](recordset-object-ado.md) に対して呼び出すと、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="30d0f-112">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

