---
title: datecreated プロパティプロパティ (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5dc326b271e8444211bba0cd2d3c37c047ac205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314540"
---
# <a name="tabledefdatecreated-property-dao"></a>datecreated プロパティプロパティ (DAO)


**適用先:** Access 2013、Office 2013

オブジェクトが作成された日付と時刻を返します (Microsoft access ワークスペースのみ)。 バリアント型 (**Variant**) の値を使用します。

## <a name="syntax"></a>構文

*式*。datecreated プロパティ

*式***TableDef**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**DateCreated** プロパティと **LastUpdated** プロパティは、それぞれオブジェクトが作成された日時、最後に更新された日時を返します。マルチユーザー環境では、DateCreated プロパティと LastUpdated プロパティの設定値が異なることを避けるために、これらの設定をファイル サーバーから直接取得する必要があります。

