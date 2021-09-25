---
title: Cancel メソッド (RDS)
TOCTitle: Cancel method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6d7c22f5b120d9685a2aae0b84eefc466bbfd7d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558610"
---
# <a name="cancel-method-rds"></a>Cancel メソッド (RDS)


**適用先:** Access 2013、Office 2013

保留中の非同期メソッド呼び出しの実行を取り消します。

## <a name="syntax"></a>構文

*RDS*. *DataControl*.キャンセル

## <a name="remarks"></a>注釈

**Cancel** を呼び出すと、[ReadyState](readystate-property-rds.md) が自動的に **adcReadyStateLoaded** に設定され、[Recordset](recordset-object-ado.md) は空になります。

