---
title: MoveFirst、MoveLast、MoveNext、および MovePrevious メソッド (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 02c6bc5ab4cc8357d7f349eb1698c2e6a026e173
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602854"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="36854-102">MoveFirst、MoveLast、MoveNext、および MovePrevious メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="36854-102">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</span></span>


<span data-ttu-id="36854-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="36854-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="36854-104">指定された [Recordset](recordset-object-ado.md) オブジェクトの最初、最後、次、または前のレコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="36854-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="36854-105">構文</span><span class="sxs-lookup"><span data-stu-id="36854-105">Syntax</span></span>

<span data-ttu-id="36854-106">*DataControl*。レコード セットです。{</span><span class="sxs-lookup"><span data-stu-id="36854-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="36854-107">MoveFirst |MoveLast |MoveNext |MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="36854-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="36854-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="36854-108">Parameters</span></span>

  - <span data-ttu-id="36854-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="36854-109">*DataControl*</span></span>

  - <span data-ttu-id="36854-110">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="36854-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="36854-111">解説</span><span class="sxs-lookup"><span data-stu-id="36854-111">Remarks</span></span>

<span data-ttu-id="36854-112"><<<<<<< ヘッドを使用できます、 **Move**メソッド**rds.DataControl** Web ページ上のデータ バインド コントロール内のデータ レコード間を移動するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="36854-112"><<<<<<< HEAD You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a Web page.</span></span> <span data-ttu-id="36854-113">たとえば、 **RDS.DataControl** オブジェクトにバインドしてグリッドに **Recordset** を表示しているとします。</span><span class="sxs-lookup"><span data-stu-id="36854-113">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="36854-114">[First]、[Last]、[Next]、および [Previous] ボタンを追加し、ユーザーが各ボタンをクリックすると、表示されている **Recordset** の最初、最後、次、または前のレコードに移動できるようにします。</span><span class="sxs-lookup"><span data-stu-id="36854-114">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="36854-115">これを行うには、[First]、[Last]、[Next]、および [Previous] の各ボタンの onClick プロシージャで、 **RDS.DataControl** オブジェクトの **MoveFirst** 、 **MoveLast** 、 **MoveNext** 、および **MovePrevious** の各メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="36854-115">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="36854-116">「 [Address Book のナビゲーション ボタン](address-book-navigation-buttons.md)」でこの方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="36854-116">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>
<span data-ttu-id="36854-117">=== を使用できます、 **Move**メソッド**rds.DataControl** web ページ上のデータ バインド コントロール内のデータ レコード間を移動するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="36854-117">======= You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> <span data-ttu-id="36854-118">たとえば、 **RDS.DataControl** オブジェクトにバインドしてグリッドに **Recordset** を表示しているとします。</span><span class="sxs-lookup"><span data-stu-id="36854-118">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="36854-119">[First]、[Last]、[Next]、および [Previous] ボタンを追加し、ユーザーが各ボタンをクリックすると、表示されている **Recordset** の最初、最後、次、または前のレコードに移動できるようにします。</span><span class="sxs-lookup"><span data-stu-id="36854-119">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="36854-120">これを行うには、[First]、[Last]、[Next]、および [Previous] の各ボタンの onClick プロシージャで、 **RDS.DataControl** オブジェクトの **MoveFirst** 、 **MoveLast** 、 **MoveNext** 、および **MovePrevious** の各メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="36854-120">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="36854-121">「 [Address Book のナビゲーション ボタン](address-book-navigation-buttons.md)」でこの方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="36854-121">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>
>>>>>>> <span data-ttu-id="36854-122">master</span><span class="sxs-lookup"><span data-stu-id="36854-122">master</span></span>

