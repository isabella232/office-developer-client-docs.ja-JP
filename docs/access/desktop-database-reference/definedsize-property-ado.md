---
title: DefinedSize プロパティ (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 121e81734fc5ecc0a761dae53942f1cbed98df2a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715327"
---
# <a name="definedsize-property-ado"></a><span data-ttu-id="d6012-102">DefinedSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="d6012-102">DefinedSize property (ADO)</span></span>


<span data-ttu-id="d6012-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d6012-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6012-104">[Field](field-object-ado.md) オブジェクトのデータ容量を示します。</span><span class="sxs-lookup"><span data-stu-id="d6012-104">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6012-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="d6012-105">Return value</span></span>

<span data-ttu-id="d6012-106">バイト数でフィールドの定義サイズを反映する長整数型 ( **Long** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="d6012-106">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6012-107">解説</span><span class="sxs-lookup"><span data-stu-id="d6012-107">Remarks</span></span>

<span data-ttu-id="d6012-108">**DefinedSize** プロパティは、 **Field** オブジェクトのデータ容量を調べるために使います。</span><span class="sxs-lookup"><span data-stu-id="d6012-108">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="d6012-p101">**DefinedSize** プロパティと [ActualSize](actualsize-property-ado.md) プロパティは異なるものです。たとえば、宣言タイプが **adVarChar** で **DefinedSize** プロパティ値が 50 の、1 文字を格納した **Field** オブジェクトがあるとします。このオブジェクトが返す **ActualSize** プロパティ値は、1 文字をバイト数で表した長さです。</span><span class="sxs-lookup"><span data-stu-id="d6012-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

