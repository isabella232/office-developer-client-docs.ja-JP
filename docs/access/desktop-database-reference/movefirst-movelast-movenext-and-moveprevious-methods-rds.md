---
title: MoveFirst、MoveLast、MoveNext、および MovePrevious メソッド (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4671e57e3edb44bc1c927ca11f2cf79e70c2699
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478094"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="d90b0-102">MoveFirst、MoveLast、MoveNext、および MovePrevious メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="d90b0-102">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</span></span>


<span data-ttu-id="d90b0-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d90b0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d90b0-104">指定された [Recordset](recordset-object-ado.md) オブジェクトの最初、最後、次、または前のレコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="d90b0-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d90b0-105">構文</span><span class="sxs-lookup"><span data-stu-id="d90b0-105">Syntax</span></span>

<span data-ttu-id="d90b0-106">*DataControl*。レコード セットです。{</span><span class="sxs-lookup"><span data-stu-id="d90b0-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="d90b0-107">MoveFirst |MoveLast |MoveNext |MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="d90b0-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="d90b0-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d90b0-108">Parameters</span></span>

  - <span data-ttu-id="d90b0-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="d90b0-109">*DataControl*</span></span>

  - <span data-ttu-id="d90b0-110">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d90b0-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d90b0-111">解説</span><span class="sxs-lookup"><span data-stu-id="d90b0-111">Remarks</span></span>

<span data-ttu-id="d90b0-p102">**RDS.DataControl** オブジェクトで **Move** メソッドを使用すると、Web ページ上のデータ連結コントロールのデータ レコード間を移動できます。たとえば、 **RDS.DataControl** オブジェクトにバインドしてグリッドに **Recordset** を表示しているとします。[First]、[Last]、[Next]、および [Previous] ボタンを追加し、ユーザーが各ボタンをクリックすると、表示されている **Recordset** の最初、最後、次、または前のレコードに移動できるようにします。これを行うには、[First]、[Last]、[Next]、および [Previous] の各ボタンの onClick プロシージャで、 **RDS.DataControl** オブジェクトの **MoveFirst** 、 **MoveLast** 、 **MoveNext** 、および **MovePrevious** の各メソッドを呼び出します。「 [Address Book のナビゲーション ボタン](address-book-navigation-buttons.md)」でこの方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="d90b0-p102">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a Web page. For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object. You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**. You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively. The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

