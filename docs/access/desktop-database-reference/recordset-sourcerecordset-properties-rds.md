---
title: Recordset プロパティと SourceRecordset プロパティ (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21176e050c77b0f14fcb03b054e8a1ab692df7d5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949258"
---
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="d55c9-102">Recordset プロパティと SourceRecordset プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="d55c9-102">Recordset, SourceRecordset properties (RDS)</span></span>

<span data-ttu-id="d55c9-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d55c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d55c9-104">カスタム ビジネス オブジェクトから返された **Recordset** オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="d55c9-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d55c9-105">構文</span><span class="sxs-lookup"><span data-stu-id="d55c9-105">Syntax</span></span>

<span data-ttu-id="d55c9-106">*DataControl*。SourceRecordset =*レコード セット*</span><span class="sxs-lookup"><span data-stu-id="d55c9-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="d55c9-107">*レコード セット* = *DataControl*。レコード セット</span><span class="sxs-lookup"><span data-stu-id="d55c9-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="d55c9-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d55c9-108">Parameters</span></span>

|<span data-ttu-id="d55c9-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d55c9-109">Parameter</span></span>|<span data-ttu-id="d55c9-110">説明</span><span class="sxs-lookup"><span data-stu-id="d55c9-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d55c9-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="d55c9-111">*DataControl*</span></span> |<span data-ttu-id="d55c9-112">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d55c9-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="d55c9-113">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="d55c9-113">*Recordset*</span></span> |<span data-ttu-id="d55c9-114">**Recordset** オブジェクトを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="d55c9-114">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d55c9-115">解説</span><span class="sxs-lookup"><span data-stu-id="d55c9-115">Remarks</span></span>

<span data-ttu-id="d55c9-116">**SourceRecordset** プロパティをカスタム ビジネス オブジェクトから返される [Recordset](recordset-object-ado.md) に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d55c9-116">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="d55c9-p101">これらのプロパティを使用すると、カスタム プロセスによってバインド処理を実行できます。これらのプロパティは **Recordset** にラップされた行セットを受け取るので、 **Recordset** を直接操作して、プロパティの設定や **Recordset** の反復処理などの操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="d55c9-p101">These properties allow an application to handle the binding process by means of a custom process. They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="d55c9-119">**SourceRecordset** プロパティの値の設定や **Recordset** プロパティの値の取得は、実行時にスクリプト コードで行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d55c9-119">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="d55c9-120">値の取得のみ可能なプロパティである **Recordset** プロパティとは対照的に、 **SourceRecordset** は値の設定のみ可能なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="d55c9-120">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>

