---
title: SubmitChanges メソッド (RDS)
TOCTitle: SubmitChanges Method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 521728af91967d673a1c69f4e4812b0aaa73ce59
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883884"
---
# <a name="submitchanges-method-rds"></a><span data-ttu-id="2a77e-102">SubmitChanges メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="2a77e-102">SubmitChanges Method (RDS)</span></span>


<span data-ttu-id="2a77e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2a77e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a77e-104">ローカルにキャッシュされていて更新可能な [Recordset](recordset-object-ado.md) の保留中の変更を、 [Connect](connect-property-rds.md) プロパティまたは [URL](url-property-rds.md) プロパティで指定されているデータ ソースに送信します。</span><span class="sxs-lookup"><span data-stu-id="2a77e-104">Submits pending changes of the locally cached and updatable [Recordset](recordset-object-ado.md) to the data source specified in the [Connect](connect-property-rds.md) property or the [URL](url-property-rds.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a77e-105">構文</span><span class="sxs-lookup"><span data-stu-id="2a77e-105">Syntax</span></span>

<span data-ttu-id="2a77e-106">*DataControl*。SubmitChanges</span><span class="sxs-lookup"><span data-stu-id="2a77e-106">*DataControl*.SubmitChanges</span></span>

<span data-ttu-id="2a77e-107">*DataFactory*。SubmitChanges*接続*、*レコード セット*</span><span class="sxs-lookup"><span data-stu-id="2a77e-107">*DataFactory*.SubmitChanges*Connection*, *Recordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="2a77e-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2a77e-108">Parameters</span></span>

  - <span data-ttu-id="2a77e-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="2a77e-109">*DataControl*</span></span>

  - <span data-ttu-id="2a77e-110">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数。</span><span class="sxs-lookup"><span data-stu-id="2a77e-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="2a77e-111">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="2a77e-111">*DataFactory*</span></span>

  - <span data-ttu-id="2a77e-112">[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a77e-112">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="2a77e-113">*Connection*</span><span class="sxs-lookup"><span data-stu-id="2a77e-113">*Connection*</span></span>

  - <span data-ttu-id="2a77e-114">**RDS.DataControl** オブジェクトの **Connect** プロパティで作成された接続を表す文字列型 ( **String** ) の値。</span><span class="sxs-lookup"><span data-stu-id="2a77e-114">A **String** value that represents the connection created with the **RDS.DataControl** object's **Connect** property.</span></span>

  - <span data-ttu-id="2a77e-115">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="2a77e-115">*Recordset*</span></span>

  - <span data-ttu-id="2a77e-116">**Recordset** オブジェクトを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="2a77e-116">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a77e-117">解説</span><span class="sxs-lookup"><span data-stu-id="2a77e-117">Remarks</span></span>

<span data-ttu-id="2a77e-118">[RDS.DataControl](connect-property-rds.md) オブジェクトで [SubmitChanges](server-property-rds.md) メソッドを使用するには、その前に [Connect](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) プロパティ、 **Server** プロパティ、および **SQL** プロパティを設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a77e-118">The [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) properties must be set before you can use the **SubmitChanges** method with the **RDS.DataControl** object.</span></span>

<span data-ttu-id="2a77e-119">[SubmitChanges](cancelupdate-method-rds.md) を呼び出した後に同じ **Recordset** オブジェクトに対して **CancelUpdate** メソッドを呼び出しても、既に変更がコミットされているため、その **CancelUpdate** 呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="2a77e-119">If you call the [CancelUpdate](cancelupdate-method-rds.md) method after you have called **SubmitChanges** for the same **Recordset** object, the **CancelUpdate** call fails because the changes have already been committed.</span></span>

<span data-ttu-id="2a77e-120">変更を加えられたレコードだけが変更を反映させるために送信され、すべての変更が成功するか、またはすべてまとめて失敗します。</span><span class="sxs-lookup"><span data-stu-id="2a77e-120">Only the changed records are sent for modification, and either all of the changes succeed or all of them fail together.</span></span>

<span data-ttu-id="2a77e-121">**SubmitChanges**は、*既定*の**RDSServer.DataFactory**オブジェクトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a77e-121">You can use **SubmitChanges** only with the *default* **RDSServer.DataFactory** object.</span></span> <span data-ttu-id="2a77e-122">カスタム ビジネス オブジェクトには、このメソッドは使用できません。</span><span class="sxs-lookup"><span data-stu-id="2a77e-122">Custom business objects can't use this method.</span></span>

<span data-ttu-id="2a77e-123">**URL** プロパティが設定されている場合、 **SubmitChanges** は、その URL で指定された場所に変更内容を送信します。</span><span class="sxs-lookup"><span data-stu-id="2a77e-123">If the **URL** property has been set, **SubmitChanges** will submit changes to the location specified by the URL.</span></span>

