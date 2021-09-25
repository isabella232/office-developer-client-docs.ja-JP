---
title: TRANSACTION ステートメント (Microsoft Access SQL)
TOCTitle: TRANSACTION statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: e3ed36a0805754f15527b476528d875fa4844dcf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601647"
---
# <a name="transaction-statement-microsoft-access-sql"></a>TRANSACTION ステートメント (Microsoft Access SQL)

**適用先:** Access 2013、Office 2013

明示的なトランザクションを開始および終了するために使用します。

## <a name="syntax"></a>構文

**新しいトランザクションを開始します**:

BEGIN TRANSACTION

**トランザクションの処理中に行われたすべての仕事をコミットして、トランザクションを終了します**:

COMMIT \[TRANSACTION | WORK\]

**トランザクションの処理中に行われたすべての仕事をロールバックして、トランザクションを終了します**:

ROLLBACK \[TRANSACTION | WORK\]

## <a name="remarks"></a>注釈

トランザクションは自動的に開始しません。トランザクションを開始するには、BEGIN TRANSACTION を使用して明示的に開始する必要があります。

トランザクションは最大 5 レベルまで入れ子にすることができます。入れ子になったトランザクションを開始するには、既存のトランザクションのコンテキスト内で BEGIN TRANSACTION を使用します。

トランザクションはリンク テーブルではサポートされていません。

