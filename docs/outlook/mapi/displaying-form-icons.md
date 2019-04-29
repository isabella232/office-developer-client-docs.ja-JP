---
title: フォームアイコンの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438632"
---
# <a name="displaying-form-icons"></a>フォームアイコンの表示

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダー内のメッセージの一覧を表示する場合、メッセージを標準の IPM のカスタムメッセージクラスと区別すると、ユーザーにとって便利です。メッセージを確認します。 カスタムメッセージクラスはフォームサーバーに対応しており、フォームサーバーはそれ自体を表すアイコンを提供します。 これらのアイコンをメッセージ一覧に表示して、ユーザーがメッセージを開く前に各メッセージのメッセージクラスに通知することができます。 通常、フォームの**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティのアイコンは、メッセージ一覧に表示される必要のあるものです。 フォームには、プロパティシートでフォームが最小化されているときに表示できる**PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティもあります。
  
 **そのメッセージクラスのフォームサーバーをアクティブ化せずに、メッセージクラスのアイコンを取得するには**
  
1. [imapiformmgr:: openformcontainer](imapiformmgr-openformcontainer.md)メソッドを呼び出して、 [imapiformmgr: IUnknown](imapiformcontaineriunknown.md)インターフェイスへのポインターを取得します。 
    
2. imapiformcontainer [:: ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)メソッドを呼び出して、imapiformcontainer [: imapiprop](imapiforminfoimapiprop.md)インターフェイスへのポインターを取得します。 
    
3. [imapiforminfo:: makeiconfrombinary](imapiforminfo-makeiconfrombinary.md)メソッドを呼び出して、アイコンハンドルを取得します。 
    
このアイコンは、標準の Win32 api を使用して表示できます。
  
> [!IMPORTANT]
> メッセージクラスのアイコンを取得したら、そのアイコンをキャッシュするためにすべての作業を行います。 キャッシュされていないアイコンは、クライアントアプリケーションのパフォーマンスに重大な影響を及ぼします。 アイコンをキャッシュするときは、メッセージクラスとそのサブクラスの関係に注意してください。 たとえば、IPM.注: 取り消しメッセージクラスが発生して、IPM に再度解決します。注: IPM のすべてのサブクラスが想定されているわけではありません。注: IPM のアイコンを使用する必要があります。こと. 
  

