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
ms.openlocfilehash: 6d93fc90beded30d96b4db54c35ab3046da06899
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862666"
---
# <a name="transaction-statement-microsoft-access-sql"></a>トランザクション ステートメント (Microsoft Access SQL)

**適用されます**Access 2013 |。Office 2013

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

