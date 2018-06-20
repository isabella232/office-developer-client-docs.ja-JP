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
ms.openlocfilehash: 95ef351e4fe906608319a3e25de8f20a44e23d9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800201"
---
# <a name="handling-table-notification"></a>テーブルの通知を処理します。

**適用されます**: Outlook 
  
アドバイズ ソース オブジェクト、フォルダーなど、ユーザーがメッセージを直接登録する代わりにクライアントは、内容の通知を登録できますか、階層テーブルです。 アドレスへの変更の追跡エントリ、フォルダー、および、内容を経由してメッセージを予約するか、階層テーブルは、個々 のオブジェクトをより簡単より単純です。 

たとえば、いずれかのサブフォルダーに変更が発生したときを検出するフォルダーの階層テーブルで[IMAPITable::Advise](imapitable-advise.md)を呼び出すことができます。 リモート メッセージの表示をサポートする場合は、トランスポート プロバイダーによって処理され、MAPI スプーラーを観察する状態テーブルに登録します。 
  
ただし、それは常にオブジェクトの通知ではなくテーブルの通知を使用することをお勧めします。 クライアント可能性がありますフォルダーによって実装されているテーブルではなくフォルダーにオブジェクトの通知を登録する必要がある場合の例ではフォルダー内のメッセージの数の変更を監視します。
  

