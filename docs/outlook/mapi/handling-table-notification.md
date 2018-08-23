---
title: テーブルの通知を処理します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b36e4697bfd4360f4ea6ea47c70eaaae434696d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595133"
---
# <a name="handling-table-notification"></a>テーブルの通知を処理します。

**適用されます**: Outlook 2013 |Outlook 2016 
  
アドバイズ ソース オブジェクト、フォルダーなど、ユーザーがメッセージを直接登録する代わりにクライアントは、内容の通知を登録できますか、階層テーブルです。 アドレスへの変更の追跡エントリ、フォルダー、および、内容を経由してメッセージを予約するか、階層テーブルは、個々 のオブジェクトをより簡単より単純です。 

たとえば、いずれかのサブフォルダーに変更が発生したときを検出するフォルダーの階層テーブルで[IMAPITable::Advise](imapitable-advise.md)を呼び出すことができます。 リモート メッセージの表示をサポートする場合は、トランスポート プロバイダーによって処理され、MAPI スプーラーを観察する状態テーブルに登録します。 
  
ただし、それは常にオブジェクトの通知ではなくテーブルの通知を使用することをお勧めします。 クライアント可能性がありますフォルダーによって実装されているテーブルではなくフォルダーにオブジェクトの通知を登録する必要がある場合の例ではフォルダー内のメッセージの数の変更を監視します。
  

