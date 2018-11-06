---
title: Property.Value プロパティ (DAO)
TOCTitle: Value Property
ms:assetid: 26e47b3a-4f70-27b5-2498-b44ce4dfc99f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191905(v=office.15)
ms:contentKeyID: 48543824
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052994
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4eb1a961a91bf32a69154a1f0e7b734dd00f24b6
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998897"
---
# <a name="propertyvalue-property-dao"></a><span data-ttu-id="19005-102">Property.Value プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="19005-102">Property.Value property (DAO)</span></span>

<span data-ttu-id="19005-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="19005-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19005-p101">オブジェクトの値を設定します。値の取得および設定が可能です。バリアント型 ( **Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="19005-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="19005-106">構文</span><span class="sxs-lookup"><span data-stu-id="19005-106">Syntax</span></span>

<span data-ttu-id="19005-107">*式*です。値</span><span class="sxs-lookup"><span data-stu-id="19005-107">*expression* .Value</span></span>

<span data-ttu-id="19005-108">\*式\***Property**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="19005-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="19005-109">注釈</span><span class="sxs-lookup"><span data-stu-id="19005-109">Remarks</span></span>

<span data-ttu-id="19005-110">設定値または戻り値は、オブジェクトの **Type** プロパティに指定されているデータ型に対して適切な値として評価されるバリアント型 (Variant) の値です。</span><span class="sxs-lookup"><span data-stu-id="19005-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="19005-111">通常、 **Value** プロパティは **Recordset** オブジェクトのデータを取得および変更するのに使用します。</span><span class="sxs-lookup"><span data-stu-id="19005-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="19005-p102">**Value** プロパティは、 **Field**、 **Parameter**、および **Property** の各オブジェクトの既定のプロパティです。このため、 **Value** プロパティを指定する代わりに、プロパティを直接参照してこれらのオブジェクトいずれかの値を設定または取得できます。</span><span class="sxs-lookup"><span data-stu-id="19005-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="19005-114">不適切なコンテキスト (たとえば、 **TableDef** オブジェクトの **Fields** コレクションの **Field** オブジェクトの **Value** プロパティ) で **Value** プロパティを設定または取得しようとすると、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="19005-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>

> [!NOTE]
> <span data-ttu-id="19005-115">Microsoft SQL Server データベースから小数の値を取得する場合、これらの値は Microsoft Access ワークスペースで指数表記を使用して書式設定されますが、ODBCDirect ワークスペースでは通常の少数の値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="19005-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


