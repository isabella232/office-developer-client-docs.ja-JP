---
title: Recordset プロパティおよび SourceRecordset プロパティ (RDS)
TOCTitle: Recordset, SourceRecordset Properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 08fe0f569b36fe0b3403cb564dc53eadf2edff8c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887181"
---
# <a name="recordset-sourcerecordset-properties-rds"></a><span data-ttu-id="2aca4-102">Recordset プロパティおよび SourceRecordset プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="2aca4-102">Recordset, SourceRecordset Properties (RDS)</span></span>


<span data-ttu-id="2aca4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2aca4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2aca4-104">カスタム ビジネス オブジェクトから返された **Recordset** オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="2aca4-104">Indicates the **Recordset** object returned from a custom business object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aca4-105">構文</span><span class="sxs-lookup"><span data-stu-id="2aca4-105">Syntax</span></span>

<span data-ttu-id="2aca4-106">*DataControl*。SourceRecordset =*レコード セット*</span><span class="sxs-lookup"><span data-stu-id="2aca4-106">*DataControl*.SourceRecordset = *Recordset*</span></span>

<span data-ttu-id="2aca4-107">*レコード セット* = *DataControl*。レコード セット</span><span class="sxs-lookup"><span data-stu-id="2aca4-107">*Recordset* = *DataControl*.Recordset</span></span>

## <a name="parameters"></a><span data-ttu-id="2aca4-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2aca4-108">Parameters</span></span>

  - <span data-ttu-id="2aca4-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="2aca4-109">*DataControl*</span></span>

  - <span data-ttu-id="2aca4-110">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2aca4-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="2aca4-111">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="2aca4-111">*Recordset*</span></span>

  - <span data-ttu-id="2aca4-112">**Recordset** オブジェクトを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="2aca4-112">An object variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aca4-113">解説</span><span class="sxs-lookup"><span data-stu-id="2aca4-113">Remarks</span></span>

<span data-ttu-id="2aca4-114">**SourceRecordset** プロパティをカスタム ビジネス オブジェクトから返される [Recordset](recordset-object-ado.md) に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2aca4-114">You can set the **SourceRecordset** property to a [Recordset](recordset-object-ado.md) returned from a custom business object.</span></span>

<span data-ttu-id="2aca4-p101">これらのプロパティを使用すると、カスタム プロセスによってバインド処理を実行できます。これらのプロパティは **Recordset** にラップされた行セットを受け取るので、 **Recordset** を直接操作して、プロパティの設定や **Recordset** の反復処理などの操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="2aca4-p101">These properties allow an application to handle the binding process by means of a custom process. They receive a rowset wrapped in a **Recordset** so that you can interact directly with the **Recordset**, performing actions such as setting properties or iterating through the **Recordset**.</span></span>

<span data-ttu-id="2aca4-117">**SourceRecordset** プロパティの値の設定や **Recordset** プロパティの値の取得は、実行時にスクリプト コードで行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2aca4-117">You can set the **SourceRecordset** property or read the **Recordset** property at run time in scripting code.</span></span>

<span data-ttu-id="2aca4-118">値の取得のみ可能なプロパティである **Recordset** プロパティとは対照的に、 **SourceRecordset** は値の設定のみ可能なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="2aca4-118">**SourceRecordset** is a write-only property, in contrast to the **Recordset** property, which is a read-only property.</span></span>

