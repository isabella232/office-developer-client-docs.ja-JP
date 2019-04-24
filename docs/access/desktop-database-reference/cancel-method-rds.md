---
title: Cancel メソッド (RDS)
TOCTitle: Cancel method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 35322ec058d31f92288fd06a4e8434a4256c2d74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296648"
---
# <a name="cancel-method-rds"></a>Cancel メソッド (RDS)


**適用先:** Access 2013、Office 2013

保留中の非同期メソッド呼び出しの実行を取り消します。

## <a name="syntax"></a>構文

*RDS*。 *DataControl*。キャンセル

## <a name="remarks"></a>注釈

**Cancel** を呼び出すと、[ReadyState](readystate-property-rds.md) が自動的に **adcReadyStateLoaded** に設定され、[Recordset](recordset-object-ado.md) は空になります。

