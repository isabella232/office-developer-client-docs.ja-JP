---
title: Document.LastUpdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d8d3c235efc2e1330dcbdf483bfa37be7219f64d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565486"
---
# <a name="documentlastupdated-property-dao"></a>Document.LastUpdated プロパティ (DAO)


**適用先:** Access 2013、Office 2013

オブジェクトを最後に変更した日付および時刻を取得します。値の取得のみ可能です。バリアント型 ( **Variant** ) の値を使用します。  

## <a name="syntax"></a>構文

*式* .LastUpdated

*式* Document オブジェクトを表す **変数** 。

## <a name="remarks"></a>注釈

**DateCreated** プロパティと **LastUpdated** プロパティは、それぞれオブジェクトが作成された日時、最後に更新された日時を返します。マルチユーザー環境では、DateCreated プロパティと LastUpdated プロパティの設定値が異なることを避けるために、これらの設定をファイル サーバーから直接取得する必要があります。

