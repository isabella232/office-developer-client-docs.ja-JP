---
title: ActualSize プロパティ (ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c13cb41299ddaf786e6412e43a50b1414ad818b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280433"
---
# <a name="actualsize-property-ado"></a><span data-ttu-id="d38dd-102">ActualSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="d38dd-102">ActualSize property (ADO)</span></span>

<span data-ttu-id="d38dd-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d38dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d38dd-104">フィールドの値の実際の長さを示します。</span><span class="sxs-lookup"><span data-stu-id="d38dd-104">Indicates the actual length of a field's value.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d38dd-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="d38dd-105">Settings and return values</span></span>

<span data-ttu-id="d38dd-p101">長整数型 ( **Long** ) の値を返します。プロバイダーによっては、このプロパティを BLOB データの予約空間に設定することができる場合もあり、この場合の既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="d38dd-p101">Returns a **Long** value. Some providers may allow this property to be set to reserve space for BLOB data, in which case the default value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="d38dd-108">注釈</span><span class="sxs-lookup"><span data-stu-id="d38dd-108">Remarks</span></span>

<span data-ttu-id="d38dd-p102">**ActualSize** プロパティを使用すると、[Field](field-object-ado.md) オブジェクトの値の実際の長さを取得できます。どのフィールドについても、**ActualSize** プロパティは値の取得のみ可能です。ADO が **Field** オブジェクトの値の長さを判断できない場合は、**ActualSize** プロパティからは **adUnknown** が返されます。</span><span class="sxs-lookup"><span data-stu-id="d38dd-p102">Use the **ActualSize** property to return the actual length of a [Field](field-object-ado.md) object's value. For all fields, the **ActualSize** property is read-only. If ADO cannot determine the length of the **Field** object's value, the **ActualSize** property returns **adUnknown**.</span></span>

<span data-ttu-id="d38dd-112">**ActualSize**プロパティと[未定義サイズ](definedsize-property-ado.md)プロパティは異なります。</span><span class="sxs-lookup"><span data-stu-id="d38dd-112">The **ActualSize** and [DefinedSize](definedsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="d38dd-113">**adVarChar** 型で宣言された **Field** オブジェクトで最大長が 50 文字の場合、 **DefinedSize** プロパティは 50 という値を返しますが、 **ActualSize** プロパティは、カレント レコードのそのフィールドに格納されているデータの長さを返します。</span><span class="sxs-lookup"><span data-stu-id="d38dd-113">A **Field** object with a declared type of **adVarChar** and a maximum length of 50 characters returns a **DefinedSize** property value of 50, but the **ActualSize** property value it returns is the length of the data stored in the field for the current record.</span></span> <span data-ttu-id="d38dd-114">255 バイトより大きい **DefinedSize** を持つ **Fields** は、可変長列として扱われます。</span><span class="sxs-lookup"><span data-stu-id="d38dd-114">**Fields** with a **DefinedSize** greater than 255 bytes are treated as variable length columns.</span></span>

