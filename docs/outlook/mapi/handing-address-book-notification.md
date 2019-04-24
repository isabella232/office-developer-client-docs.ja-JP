---
title: アドレス帳通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299504"
---
# <a name="handing-address-book-notification"></a>アドレス帳通知の処理
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳の通知により、クライアントは、アドレス帳のエントリまたは特定のエントリに発生するイベントを知ることができます。 これらの通知は、 [IAddrBook:: advise](iaddrbook-advise.md)を呼び出すことによって、またはアドレス帳コンテナーの hierarchy または contents テーブルによって、 [IMAPITable:: advise](imapitable-advise.md)を呼び出すことによって登録できます。 
  
特定のエントリに対して登録する場合は、アドレス帳のコンテナー、配布リスト、またはメッセージングユーザーのエントリ識別子を指定し、アドレス帳全体に通知を登録する場合は NULL を指定します。 エントリ識別子は、アドレス帳コンテナー内のメッセージングユーザーまたは配布リストを表す必要があります。 **IAddrBook:: advise**は、このエントリ識別子を調べて、対応するオブジェクトをどのアドレス帳プロバイダーが担当しているかを判断し、その呼び出しを適切なアドレス帳プロバイダーの[IABLogon:: advise](iablogon-advise.md)メソッドに転送します。 
  
クライアントは、アドレス帳のエントリに次の種類のイベントを登録できます。
  
- 重大なエラー
    
- 任意のオブジェクトイベント (作成、変更、削除、移動、またはコピー)
    
- 変更されたテーブル
    
通常、登録はアドレス帳のコンテナーの内容と階層テーブルに対してのみ行われます。 クライアントが低レベルのメッセージングユーザーおよび配布リストオブジェクトに登録することはまれです。 理由は次のとおりです。
  
- 多くのアドレス帳プロバイダーは、メッセージングユーザーおよび配布リストに対する通知をサポートしていません。
    
- テーブル通知は、変更を追跡してユーザーに報告するのに十分です。
    

