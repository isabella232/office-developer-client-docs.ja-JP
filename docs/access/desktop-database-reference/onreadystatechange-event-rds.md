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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288491"
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

