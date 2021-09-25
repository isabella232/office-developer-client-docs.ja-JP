---
title: TableDef.Updatable プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ab21e5493b1c0c3c2d1ef0cf3fffb9a9d4ff965a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580749"
---
# <a name="tabledefupdatable-property-dao"></a>TableDef.Updatable プロパティ (DAO)


**適用先:** Access 2013、Office 2013

DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean** ) の値を使用します。  

## <a name="syntax"></a>構文

*式* .更新可能

*式***TableDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**Updatable** プロパティの設定値は常に、新しく作成した **TableDef** オブジェクトでは **True**、リンクされた **TableDef** オブジェクトでは **False** となります。新しい **TableDef** オブジェクトは、現在のユーザーが書き込み権限を持つデータベースにのみ追加できます。

