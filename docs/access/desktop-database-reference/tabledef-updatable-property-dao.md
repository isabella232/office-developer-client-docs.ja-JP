---
title: TableDef.Updatable プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44f24e68b60f69304a167d2b9b5ce0b4b0e69b11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479544"
---
# <a name="tabledefupdatable-property-dao"></a>TableDef.Updatable プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。更新可能です

*式***テーブル定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Updatable** プロパティの設定値は常に、新しく作成した **TableDef** オブジェクトでは **True**、リンクされた **TableDef** オブジェクトでは **False** となります。新しい **TableDef** オブジェクトは、現在のユーザーが書き込み権限を持つデータベースにのみ追加できます。

