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
localization_priority: Priority
ms.openlocfilehash: 828bccfad83320d27f9473d532ab86f73b2fde98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314148"
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

