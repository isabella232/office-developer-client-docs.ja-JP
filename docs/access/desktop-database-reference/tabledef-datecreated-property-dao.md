---
title: TableDef.DateCreated プロパティ (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2cf97df5d5861a3bb0fdac34ceabc8f732a87d5c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885599"
---
# <a name="tabledefdatecreated-property-dao"></a>TableDef.DateCreated プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

オブジェクトを作成した日付と時刻を取得します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。バリアント型 ( **Variant**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。作成日時

*式***テーブル定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**DateCreated** プロパティおよび **LastUpdated** プロパティは、オブジェクトが作成された日付および時刻、または最後に更新された日付および時刻を取得します。マルチユーザー環境では、ユーザーがファイル サーバーから直接これらの設定を取得し、DateCreated プロパティおよび LastUpdated プロパティの設定値が一致しなくなるのを防ぐ必要があります。

