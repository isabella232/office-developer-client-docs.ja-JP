---
title: onReadyStateChange イベント (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 81e3baa586b428c28e90de68c4632a3b28e5a699
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568804"
---
# <a name="onreadystatechange-event-rds"></a>onReadyStateChange イベント (RDS)

**適用先:** Access 2013、Office 2013

**onReadyStateChange** イベントは、[ReadyState](readystate-property-rds.md) プロパティの値が変更されるたびに呼び出されます。

## <a name="syntax"></a>構文

onReadyStateChange

## <a name="parameters"></a>パラメーター

なし。

## <a name="remarks"></a>注釈

**ReadyState** プロパティは、[Recordset](recordset-object-ado.md) オブジェクトに非同期でデータを取得するときの [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの進行状況を反映します。**ReadyState** プロパティの変更が発生するたびにこの変更を監視するには、**onReadyStateChange** イベントを使用します。この方法は、定期的にプロパティの値を調べるよりも効率的です。

