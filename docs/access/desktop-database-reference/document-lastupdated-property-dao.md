---
title: 文書の lastupdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abb766f7a47cbacaededf65eb2b5e9145bf88c60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293806"
---
# <a name="documentlastupdated-property-dao"></a>文書の lastupdated プロパティ (DAO)


**適用先:** Access 2013、Office 2013

オブジェクトに対して最後に行われた変更の日付と時刻を返します。 バリアント型 (**Variant**) の値を使用します。

## <a name="syntax"></a>構文

*式*。LastUpdated

*式***Document**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**DateCreated** プロパティと **LastUpdated** プロパティは、それぞれオブジェクトが作成された日時、最後に更新された日時を返します。マルチユーザー環境では、DateCreated プロパティと LastUpdated プロパティの設定値が異なることを避けるために、これらの設定をファイル サーバーから直接取得する必要があります。

