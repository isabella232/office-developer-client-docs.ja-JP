---
title: Supports メソッド (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4aa04cf3d04b71e0a84279bfc5340e7ee326de48
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949628"
---
# <a name="supports-method-ado"></a><span data-ttu-id="e0adf-102">Supports メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="e0adf-102">Supports method (ADO)</span></span>

<span data-ttu-id="e0adf-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e0adf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0adf-104">指定された [Recordset](recordset-object-ado.md) オブジェクトが特定の種類の機能をサポートしているかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="e0adf-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0adf-105">構文</span><span class="sxs-lookup"><span data-stu-id="e0adf-105">Syntax</span></span>

<span data-ttu-id="e0adf-106">*ブール値* = *レコード セット*です。(*CursorOptions*) をサポートしています</span><span class="sxs-lookup"><span data-stu-id="e0adf-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="e0adf-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="e0adf-107">Return value</span></span>

<span data-ttu-id="e0adf-108">*CursorOptions*引数で識別される機能のすべてが、プロバイダーでサポートされているかどうかを示す**ブール**値を返します。</span><span class="sxs-lookup"><span data-stu-id="e0adf-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0adf-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e0adf-109">Parameters</span></span>

|<span data-ttu-id="e0adf-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e0adf-110">Parameter</span></span>|<span data-ttu-id="e0adf-111">説明</span><span class="sxs-lookup"><span data-stu-id="e0adf-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e0adf-112">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="e0adf-112">*CursorOptions*</span></span> |<span data-ttu-id="e0adf-113">1 つまたは複数の **CursorOptionEnum** 値から成る長整数型 ( [Long](cursoroptionenum.md) ) の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="e0adf-113">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e0adf-114">解説</span><span class="sxs-lookup"><span data-stu-id="e0adf-114">Remarks</span></span>

<span data-ttu-id="e0adf-p101">**Supports** メソッドを使用すると、**Recordset** オブジェクトでサポートされている機能の種類を調べることができます。*CursorOptions* で指定した定数に対応する機能が **Recordset** オブジェクトでサポートされていると、**Supports** メソッドは **True** を返します。それ以外の場合は、**False** を返します。</span><span class="sxs-lookup"><span data-stu-id="e0adf-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <span data-ttu-id="e0adf-p102">[!メモ] 指定した機能について **Supports** メソッドから **True** が返されても、その機能がどのような状況でもそのプロバイダーで使用できるという保証はありません。 **Supports** メソッドは、一定の条件が満たされていることを前提にしたうえで、指定された機能をプロバイダーがサポートできるかどうかを判別した結果を単に返すだけです。たとえば、カーソルが複数のテーブルの結合に基づいているために更新不可能な列があったとしても、 **Supports** は **Recordset** オブジェクトが更新をサポートしていると判別する場合があります。</span><span class="sxs-lookup"><span data-stu-id="e0adf-p102">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the **Supports** method may indicate that a **Recordset** object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span>


