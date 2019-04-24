---
title: テーブル通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299490"
---
# <a name="handling-table-notification"></a>テーブル通知の処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーやメッセージングユーザーなど、アドバイズソースオブジェクトを直接登録する代わりに、クライアントはコンテンツまたは階層テーブルに通知を登録することができます。 コンテンツまたは階層テーブルを介してアドレス帳のエントリ、フォルダー、およびメッセージに加えられた変更を追跡することは、個々のオブジェクトを使用するよりも簡単でわかりやすくなります。 

たとえば、フォルダーの階層テーブルに対して[IMAPITable:: アドバイズ](imapitable-advise.md)を呼び出して、そのサブフォルダーの1つに変更が発生したことを検出できます。 リモートメッセージの表示をサポートしている場合は、[状態] テーブルに登録して、トランスポートプロバイダーと MAPI スプーラーによるアクティビティを監視します。 
  
ただし、オブジェクト通知ではなくテーブル通知の使用を常に推奨するわけではありません。 フォルダー内のメッセージ数の変更の監視は、クライアントがフォルダーで実装されたテーブルではなく、フォルダーにオブジェクト通知を登録する必要がある場合の例です。
  

