---
title: MoveFirst メソッド、MoveLast メソッド、MoveNext メソッド、MovePrevious メソッド (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac3daa25f933438ad09b5af3c4b383bb19461cb2
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949251"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="b7ef0-102">MoveFirst メソッド、MoveLast メソッド、MoveNext メソッド、MovePrevious メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="b7ef0-102">MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)</span></span>

<span data-ttu-id="b7ef0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b7ef0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7ef0-104">指定された [Recordset](recordset-object-ado.md) オブジェクトの最初、最後、次、または前のレコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="b7ef0-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7ef0-105">構文</span><span class="sxs-lookup"><span data-stu-id="b7ef0-105">Syntax</span></span>

<span data-ttu-id="b7ef0-106">*DataControl*。レコード セットです。{</span><span class="sxs-lookup"><span data-stu-id="b7ef0-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="b7ef0-107">MoveFirst |MoveLast |MoveNext |MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="b7ef0-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="b7ef0-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b7ef0-108">Parameters</span></span>

|<span data-ttu-id="b7ef0-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b7ef0-109">Parameter</span></span>|<span data-ttu-id="b7ef0-110">説明</span><span class="sxs-lookup"><span data-stu-id="b7ef0-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b7ef0-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b7ef0-111">*DataControl*</span></span> |<span data-ttu-id="b7ef0-112">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b7ef0-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b7ef0-113">解説</span><span class="sxs-lookup"><span data-stu-id="b7ef0-113">Remarks</span></span>

<span data-ttu-id="b7ef0-114">Rds. の**に、 **Move**メソッドを使用します。DataControl** web ページ上のデータ バインド コントロール内のデータ レコード間を移動するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="b7ef0-114">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> 

<span data-ttu-id="b7ef0-115">たとえば、 **RDS.DataControl** オブジェクトにバインドしてグリッドに **Recordset** を表示しているとします。</span><span class="sxs-lookup"><span data-stu-id="b7ef0-115">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="b7ef0-116">[First]、[Last]、[Next]、および [Previous] ボタンを追加し、ユーザーが各ボタンをクリックすると、表示されている **Recordset** の最初、最後、次、または前のレコードに移動できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b7ef0-116">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="b7ef0-117">これを行うには、[First]、[Last]、[Next]、および [Previous] の各ボタンの onClick プロシージャで、 **RDS.DataControl** オブジェクトの **MoveFirst** 、 **MoveLast** 、 **MoveNext** 、および **MovePrevious** の各メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b7ef0-117">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="b7ef0-118">「 [Address Book のナビゲーション ボタン](address-book-navigation-buttons.md)」でこの方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="b7ef0-118">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

