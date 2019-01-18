---
title: onReadyStateChange イベント (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ec2104634d9158d59d488b50d543cf0e57d9bd62
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699731"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="23bd5-102">onReadyStateChange イベント (RDS)</span><span class="sxs-lookup"><span data-stu-id="23bd5-102">onReadyStateChange event (RDS)</span></span>

<span data-ttu-id="23bd5-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="23bd5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23bd5-104">**onReadyStateChange** イベントは、 [ReadyState](readystate-property-rds.md) プロパティの値が変更されるたびに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="23bd5-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="23bd5-105">構文</span><span class="sxs-lookup"><span data-stu-id="23bd5-105">Syntax</span></span>

<span data-ttu-id="23bd5-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="23bd5-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="23bd5-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23bd5-107">Parameters</span></span>

<span data-ttu-id="23bd5-108">なし。</span><span class="sxs-lookup"><span data-stu-id="23bd5-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="23bd5-109">解説</span><span class="sxs-lookup"><span data-stu-id="23bd5-109">Remarks</span></span>

<span data-ttu-id="23bd5-p101">**ReadyState** プロパティは、 [Recordset](datacontrol-object-rds.md) オブジェクトに非同期でデータを取得するときの [RDS.DataControl](recordset-object-ado.md) オブジェクトの進行状況を反映します。 **ReadyState** プロパティの変更が発生するたびにこの変更を監視するには、 **onReadyStateChange** イベントを使用します。この方法は、定期的にプロパティの値を調べるよりも効率的です。</span><span class="sxs-lookup"><span data-stu-id="23bd5-p101">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object. Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur. This is more efficient than periodically checking the property's value.</span></span>

