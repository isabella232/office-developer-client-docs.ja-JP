---
title: Supports メソッド (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42447614c5fc58bc4eb2933354908693adf68ce6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308464"
---
# <a name="supports-method-ado"></a><span data-ttu-id="51074-102">Supports メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="51074-102">Supports method (ADO)</span></span>

<span data-ttu-id="51074-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="51074-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51074-104">指定された [Recordset](recordset-object-ado.md) オブジェクトが特定の種類の機能をサポートしているかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="51074-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="51074-105">構文</span><span class="sxs-lookup"><span data-stu-id="51074-105">Syntax</span></span>

<span data-ttu-id="51074-106">*ブール値* = の*recordset*。Supports (*カーソルオプション*)</span><span class="sxs-lookup"><span data-stu-id="51074-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="51074-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="51074-107">Return value</span></span>

<span data-ttu-id="51074-108">プロバイダーが *CursorOptions* 引数で指定されたすべての機能をサポートしているかどうかを示すブール型 (**Boolean**) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="51074-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="51074-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="51074-109">Parameters</span></span>

|<span data-ttu-id="51074-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="51074-110">Parameter</span></span>|<span data-ttu-id="51074-111">説明</span><span class="sxs-lookup"><span data-stu-id="51074-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="51074-112">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="51074-112">*CursorOptions*</span></span> |<span data-ttu-id="51074-113">1 つまたは複数の **CursorOptionEnum** 値から成る長整数型 ( [Long](cursoroptionenum.md) ) の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="51074-113">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>|

## <a name="remarks"></a><span data-ttu-id="51074-114">注釈</span><span class="sxs-lookup"><span data-stu-id="51074-114">Remarks</span></span>

<span data-ttu-id="51074-p101">**Supports** メソッドを使用すると、**Recordset** オブジェクトでサポートされている機能の種類を調べることができます。*CursorOptions* で指定した定数に対応する機能が **Recordset** オブジェクトでサポートされていると、**Supports** メソッドは **True** を返します。それ以外の場合は、**False** を返します。</span><span class="sxs-lookup"><span data-stu-id="51074-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <span data-ttu-id="51074-p102">[!メモ] 指定した機能について **Supports** メソッドから **True** が返されても、その機能がどのような状況でもそのプロバイダーで使用できるという保証はありません。 **Supports** メソッドは、一定の条件が満たされていることを前提にしたうえで、指定された機能をプロバイダーがサポートできるかどうかを判別した結果を単に返すだけです。たとえば、カーソルが複数のテーブルの結合に基づいているために更新不可能な列があったとしても、 **Supports** は **Recordset** オブジェクトが更新をサポートしていると判別する場合があります。</span><span class="sxs-lookup"><span data-stu-id="51074-p102">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the **Supports** method may indicate that a **Recordset** object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span>


