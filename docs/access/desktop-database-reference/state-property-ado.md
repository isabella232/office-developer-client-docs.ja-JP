---
title: State プロパティ (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bce3f87a6530315a128396fe0e4de5390e0f47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308534"
---
# <a name="state-property-ado"></a><span data-ttu-id="a9a48-102">State プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="a9a48-102">State property (ADO)</span></span>


<span data-ttu-id="a9a48-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9a48-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9a48-104">対象になるすべてのオブジェクトについて、オブジェクトの状態が開いているか、閉じているかを示します。</span><span class="sxs-lookup"><span data-stu-id="a9a48-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="a9a48-105">非同期メソッドを実行する対象になるすべてのオブジェクトについて、オブジェクトの状態が接続、実行、取得のいずれであるかを示します。</span><span class="sxs-lookup"><span data-stu-id="a9a48-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9a48-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="a9a48-106">Return value</span></span>

<span data-ttu-id="a9a48-107">**ObjectStateEnum** の値になる長整数型 ( [Long](objectstateenum.md) ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="a9a48-107">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value.</span></span> <span data-ttu-id="a9a48-108">既定値は **adStateClosed** です。</span><span class="sxs-lookup"><span data-stu-id="a9a48-108">The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9a48-109">注釈</span><span class="sxs-lookup"><span data-stu-id="a9a48-109">Remarks</span></span>

<span data-ttu-id="a9a48-110">**State** プロパティを使用して、特定のオブジェクトの現在の状態をいつでも調べることができます。</span><span class="sxs-lookup"><span data-stu-id="a9a48-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="a9a48-p102">オブジェクトの **State** プロパティは、値の組み合わせになる場合があります。たとえば、ステートメントが実行中である場合、このプロパティの値は **adStateOpen** と **adStateExecuting** の組み合わせになります。</span><span class="sxs-lookup"><span data-stu-id="a9a48-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="a9a48-113">**State** プロパティは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="a9a48-113">The **State** property is read-only.</span></span>

