---
title: TRANSACTION ステートメント (Microsoft Access SQL)
TOCTitle: TRANSACTION Statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 13628ee6d384430691475eb06dbbbdce4e980103
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478000"
---
# <a name="transaction-statement-microsoft-access-sql"></a>TRANSACTION ステートメント (Microsoft Access SQL)


**適用されます**Access 2013 |。Office 2013

明示的なトランザクションの開始と終了に使用します。

## <a name="syntax"></a>構文

新しいトランザクションを開始します。

BEGIN TRANSACTION

トランザクションの処理中に行われたすべての仕事をコミットすることで、トランザクションを終了します。

コミット\[トランザクション。作業\]

トランザクションの処理中に行われたすべての仕事をロールバックすることで、トランザクションを終了します。

ロールバック\[トランザクション。作業\]

## <a name="remarks"></a>解説

トランザクションは自動的に開始されません。トランザクションを始めるためには、BEGIN TRANSACTION 句を使用して明示的に開始する必要があります。

トランザクションは、5 レベルの深さまでネストさせることができます。ネストさせたトランザクションを開始するには、既存のトランザクションのコンテキストの中で、BEGIN TRANSACTION 句を使用してください。

このトランザクションは、リンク テーブルには対応していません。

