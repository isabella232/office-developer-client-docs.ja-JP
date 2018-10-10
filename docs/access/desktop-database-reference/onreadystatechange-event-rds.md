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
# <a name="onreadystatechange-event-rds"></a>onReadyStateChange イベント (RDS)


**適用されます**Access 2013 |。Office 2013


**onReadyStateChange** イベントは、 [ReadyState](readystate-property-rds.md) プロパティの値が変更されるたびに呼び出されます。

## <a name="syntax"></a>構文

onReadyStateChange

## <a name="parameters"></a>パラメーター

なし。

## <a name="remarks"></a>解説

**ReadyState** プロパティは、 [Recordset](datacontrol-object-rds.md) オブジェクトに非同期でデータを取得するときの [RDS.DataControl](recordset-object-ado.md) オブジェクトの進行状況を反映します。 **ReadyState** プロパティの変更が発生するたびにこの変更を監視するには、 **onReadyStateChange** イベントを使用します。この方法は、定期的にプロパティの値を調べるよりも効率的です。

