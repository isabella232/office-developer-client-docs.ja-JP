---
title: GetChildren メソッド (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcc687e5151e95d61939c30aa4c6be4063b67c47
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931268"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="59aa1-102">GetChildren メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="59aa1-102">GetChildren method (ADO)</span></span>


<span data-ttu-id="59aa1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="59aa1-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="59aa1-104">各行がコレクション [Record](recordset-object-ado.md) の子を表す [Recordset](record-object-ado.md) を返します。</span><span class="sxs-lookup"><span data-stu-id="59aa1-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="59aa1-105">構文</span><span class="sxs-lookup"><span data-stu-id="59aa1-105">Syntax</span></span>

<span data-ttu-id="59aa1-106">\**設定\*\*\*レコード セット* = *レコード*。GetChildren</span><span class="sxs-lookup"><span data-stu-id="59aa1-106">**Set** *recordset* = *record*.GetChildren</span></span>

## <a name="return-value"></a><span data-ttu-id="59aa1-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="59aa1-107">Return value</span></span>

<span data-ttu-id="59aa1-p101">各行が現在の **Record** オブジェクトの子を表す **Recordset** オブジェクトを返します。たとえば、ディレクトリを表す **Record** の子は、親ディレクトリに含まれるファイルとサブディレクトリです。</span><span class="sxs-lookup"><span data-stu-id="59aa1-p101">A **Recordset** object for which each row represents a child of the current **Record** object. For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="59aa1-110">解説</span><span class="sxs-lookup"><span data-stu-id="59aa1-110">Remarks</span></span>

<span data-ttu-id="59aa1-p102">返される **Recordset** にどのような列があるかは、プロバイダーによって決まります。たとえば、ドキュメント ソース プロバイダーは、常にリソースの **Recordset** を返します。</span><span class="sxs-lookup"><span data-stu-id="59aa1-p102">The provider determines what columns exist in the returned **Recordset**. For example, a document source provider always returns a resource **Recordset**.</span></span>

