---
title: Parameter.Value プロパティ (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4e7f3976b934c407a038f321953259fd63a6f60
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717441"
---
# <a name="parametervalue-property-dao"></a><span data-ttu-id="43336-102">Parameter.Value プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="43336-102">Parameter.Value property (DAO)</span></span>

<span data-ttu-id="43336-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="43336-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43336-p101">オブジェクトの値を設定します。値の取得および設定が可能です。バリアント型 ( **Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="43336-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="43336-106">構文</span><span class="sxs-lookup"><span data-stu-id="43336-106">Syntax</span></span>

<span data-ttu-id="43336-107">*式*です。値</span><span class="sxs-lookup"><span data-stu-id="43336-107">*expression* .Value</span></span>

<span data-ttu-id="43336-108">\*式\***パラメーター**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="43336-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="43336-109">注釈</span><span class="sxs-lookup"><span data-stu-id="43336-109">Remarks</span></span>

<span data-ttu-id="43336-110">設定値または戻り値は、オブジェクトの **Type** プロパティに指定されているデータ型に対して適切な値として評価されるバリアント型 (Variant) の値です。</span><span class="sxs-lookup"><span data-stu-id="43336-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="43336-111">通常、 **Value** プロパティは **Recordset** オブジェクトのデータを取得および変更するのに使用します。</span><span class="sxs-lookup"><span data-stu-id="43336-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="43336-p102">**Value** プロパティは、 **Field**、 **Parameter**、および **Property** の各オブジェクトの既定のプロパティです。このため、 **Value** プロパティを指定する代わりに、プロパティを直接参照してこれらのオブジェクトいずれかの値を設定または取得できます。</span><span class="sxs-lookup"><span data-stu-id="43336-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="43336-114">不適切なコンテキスト (たとえば、 **TableDef** オブジェクトの **Fields** コレクションの **Field** オブジェクトの **Value** プロパティ) で **Value** プロパティを設定または取得しようとすると、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="43336-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>

> [!NOTE]
> <span data-ttu-id="43336-115">Microsoft SQL Server データベースから小数の値を取得する場合、これらの値は Microsoft Access ワークスペースで指数表記を使用して書式設定されますが、ODBCDirect ワークスペースでは通常の少数の値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="43336-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


