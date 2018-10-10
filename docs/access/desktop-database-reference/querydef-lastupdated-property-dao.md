---
title: QueryDef.LastUpdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37a95cefb5af5070470fb5973076e230d76c3d98
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479606"
---
# <a name="querydeflastupdated-property-dao"></a>QueryDef.LastUpdated プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

オブジェクトに対して行われた最新の変更の日付と時刻を取得します。値の取得のみ可能です。バリアント型 ( **Variant**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。LastUpdated

*式***クエリ定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**DateCreated** プロパティおよび **LastUpdated** プロパティは、オブジェクトが作成された日付および時刻、または最後に更新された日付および時刻を取得します。マルチユーザー環境では、ユーザーがファイル サーバーから直接これらの設定を取得し、DateCreated プロパティおよび LastUpdated プロパティの設定値が一致しなくなるのを防ぐ必要があります。

