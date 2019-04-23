---
title: TableDef プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314414"
---
# <a name="tabledefupdatable-property-dao"></a>TableDef プロパティ (DAO)


**適用先:** Access 2013、Office 2013

DAO オブジェクトを変更できるかどうかを示す値を返します。 値の取得のみ可能なブール型 (**Boolean**) の値です。

## <a name="syntax"></a>構文

*式*。できる

*式***TableDef**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Updatable** プロパティの設定値は常に、新しく作成した **TableDef** オブジェクトでは **True**、リンクされた **TableDef** オブジェクトでは **False** となります。新しい **TableDef** オブジェクトは、現在のユーザーが書き込み権限を持つデータベースにのみ追加できます。

