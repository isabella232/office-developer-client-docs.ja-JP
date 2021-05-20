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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435895"
---
# <a name="handling-table-notification"></a>テーブル通知の処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーやメッセージング ユーザーなどのアドバイス ソース オブジェクトに直接登録する代わりに、クライアントはコンテンツまたは階層テーブルの通知に登録できます。 コンテンツまたは階層テーブルを介してアドレス帳エントリ、フォルダー、メッセージに対する変更を追跡すると、個々のオブジェクトよりも簡単で簡単になります。 

たとえば、フォルダーの階層テーブルで [IMAPITable::Advise](imapitable-advise.md) を呼び出して、そのサブフォルダーに対する変更がいつ発生したのか確認できます。 リモート メッセージの表示をサポートしている場合は、状態テーブルに登録して、トランスポート プロバイダーと MAPI スプーラーによるアクティビティを確認します。 
  
ただし、オブジェクト通知の代わりにテーブル通知を使用することが常に望ましいとは限りではありません。 フォルダー内のメッセージ数の変更の監視は、クライアントがフォルダーによって実装されたテーブルではなく、フォルダー上のオブジェクト通知に登録する必要がある場合の例です。
  

