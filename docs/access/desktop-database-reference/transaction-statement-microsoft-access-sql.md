---
title: トランザクション ステートメント (Microsoft Access SQL)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705520"
---
# <a name="transaction-statement-microsoft-access-sql"></a>トランザクション ステートメント (Microsoft Access SQL)

**適用されます**Access 2013、Office 2013。

明示的なトランザクションの開始と終了に使用します。

## <a name="syntax"></a>構文

**新しいトランザクションを開始**します。

BEGIN TRANSACTION

**Conclude は、トランザクションをコミットすることによってすべての作業は、トランザクション中に実行**します。

コミット\[トランザクション。作業\]

**Conclude トランザクションをロールバックしてトランザクション中にすべての作業を実行**します。

ロールバック\[トランザクション。作業\]

## <a name="remarks"></a>解説

トランザクションは自動的に開始されません。トランザクションを始めるためには、BEGIN TRANSACTION 句を使用して明示的に開始する必要があります。

トランザクションは、5 レベルの深さまでネストさせることができます。ネストさせたトランザクションを開始するには、既存のトランザクションのコンテキストの中で、BEGIN TRANSACTION 句を使用してください。

このトランザクションは、リンク テーブルには対応していません。

