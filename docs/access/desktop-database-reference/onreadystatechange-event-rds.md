---
title: onReadyStateChange イベント (RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dec783aaa76745b73bd031b00f1b8587a58eb165
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478392"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="94325-102">onReadyStateChange イベント (RDS)</span><span class="sxs-lookup"><span data-stu-id="94325-102">onReadyStateChange Event (RDS)</span></span>


<span data-ttu-id="94325-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="94325-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="94325-104">**onReadyStateChange** イベントは、 [ReadyState](readystate-property-rds.md) プロパティの値が変更されるたびに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="94325-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="94325-105">構文</span><span class="sxs-lookup"><span data-stu-id="94325-105">Syntax</span></span>

<span data-ttu-id="94325-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="94325-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="94325-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="94325-107">Parameters</span></span>

<span data-ttu-id="94325-108">なし。</span><span class="sxs-lookup"><span data-stu-id="94325-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="94325-109">解説</span><span class="sxs-lookup"><span data-stu-id="94325-109">Remarks</span></span>

<span data-ttu-id="94325-p101">**ReadyState** プロパティは、 [Recordset](datacontrol-object-rds.md) オブジェクトに非同期でデータを取得するときの [RDS.DataControl](recordset-object-ado.md) オブジェクトの進行状況を反映します。 **ReadyState** プロパティの変更が発生するたびにこの変更を監視するには、 **onReadyStateChange** イベントを使用します。この方法は、定期的にプロパティの値を調べるよりも効率的です。</span><span class="sxs-lookup"><span data-stu-id="94325-p101">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object. Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur. This is more efficient than periodically checking the property's value.</span></span>

