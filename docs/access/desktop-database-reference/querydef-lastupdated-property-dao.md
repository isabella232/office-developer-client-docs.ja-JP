---
title: QueryDef.LastUpdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9938f8ff4aa6625508bdc55115f35fcff5a3e66b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617770"
---
# <a name="querydeflastupdated-property-dao"></a>QueryDef.LastUpdated プロパティ (DAO)


**適用先**: Access 2013、Office 2013

オブジェクトを最後に変更した日付および時刻を取得します。値の取得のみ可能です。バリアント型 ( **Variant** ) の値を使用します。  

## <a name="syntax"></a>構文

*式* .LastUpdated

*式* **QueryDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**DateCreated** プロパティと **LastUpdated** プロパティは、それぞれオブジェクトが作成された日時、最後に更新された日時を返します。マルチユーザー環境では、DateCreated プロパティと LastUpdated プロパティの設定値が異なることを避けるために、これらの設定をファイル サーバーから直接取得する必要があります。

