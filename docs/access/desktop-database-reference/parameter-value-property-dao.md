---
title: パラメーター Value プロパティ (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4e7f3976b934c407a038f321953259fd63a6f60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287992"
---
# <a name="parametervalue-property-dao"></a><span data-ttu-id="3396b-102">パラメーター Value プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="3396b-102">Parameter.Value property (DAO)</span></span>

<span data-ttu-id="3396b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3396b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3396b-104">オブジェクトの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="3396b-104">Sets or returns the value of an object.</span></span> <span data-ttu-id="3396b-105">値の取得と設定が可能なバリアント型 (**Variant**) の値です。</span><span class="sxs-lookup"><span data-stu-id="3396b-105">Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3396b-106">構文</span><span class="sxs-lookup"><span data-stu-id="3396b-106">Syntax</span></span>

<span data-ttu-id="3396b-107">*式*。金額</span><span class="sxs-lookup"><span data-stu-id="3396b-107">*expression* .Value</span></span>

<span data-ttu-id="3396b-108">\*式\***Parameter**オブジェクトを表す変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3396b-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3396b-109">注釈</span><span class="sxs-lookup"><span data-stu-id="3396b-109">Remarks</span></span>

<span data-ttu-id="3396b-110">設定値または戻り値は、オブジェクトの **Type** プロパティに指定されているデータ型に対して適切な値として評価されるバリアント型 (Variant) の値です。</span><span class="sxs-lookup"><span data-stu-id="3396b-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="3396b-111">通常、 **Value** プロパティは **Recordset** オブジェクトのデータを取得および変更するのに使用します。</span><span class="sxs-lookup"><span data-stu-id="3396b-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="3396b-p102">**Value** プロパティは、 **Field**、 **Parameter**、および **Property** の各オブジェクトの既定のプロパティです。このため、 **Value** プロパティを指定する代わりに、これらのオブジェクトいずれかを直接参照してその値を設定または取得できます。</span><span class="sxs-lookup"><span data-stu-id="3396b-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="3396b-114">正しくない状況で **Value** プロパティの設定または取得を行うと (たとえば、 **TableDef** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトの **Value** プロパティ)、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="3396b-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>

> [!NOTE]
> <span data-ttu-id="3396b-115">Microsoft SQL Server データベースから小数の値を取得する場合、これらの値は Microsoft Access ワークスペースで指数表記を使用して書式設定されますが、ODBCDirect ワークスペースでは通常の少数の値として表示されます。</span><span class="sxs-lookup"><span data-stu-id="3396b-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>


