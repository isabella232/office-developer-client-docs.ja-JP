---
title: Cancel メソッド (RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcd37f8736b7ab4b953480cd28daeb3080abe07f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477017"
---
# <a name="cancel-method-rds"></a>Cancel メソッド (RDS)


**適用されます**Access 2013 |。Office 2013

保留中の非同期メソッド呼び出しの実行を取り消します。

## <a name="syntax"></a>構文

*RDS*。 *DataControl*。キャンセル

## <a name="remarks"></a>解説

**Cancel** を呼び出すと、 [ReadyState](readystate-property-rds.md) が自動的に **adcReadyStateLoaded** に設定され、 [Recordset](recordset-object-ado.md) は空になります。

