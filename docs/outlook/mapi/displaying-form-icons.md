---
title: フォーム アイコンの表示
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
# <a name="displaying-form-icons"></a>フォーム アイコンの表示

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーにメッセージの一覧を表示する場合、カスタム メッセージ クラスを持つメッセージと標準 IPM を区別する場合は、ユーザーに役立ちます。メモ メッセージ。 カスタム メッセージ クラスはフォーム サーバーに対応し、フォーム サーバーは自分自身を表すアイコンを提供します。 これらのアイコンをメッセージの一覧に表示して、ユーザーがメッセージを開く前に、各メッセージのメッセージ クラスにユーザーに通知できます。 通常、メッセージの一覧にPR_MINI_ICON **(** [PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティのアイコンが表示されます。 フォームには、プロパティ **PR_ICON** でフォームを最小化するときに表示できるプロパティ [(PidTagIcon)](pidtagicon-canonical-property.md)もあります。
  
 **そのメッセージ クラスのフォーム サーバーをアクティブ化せずにメッセージ クラスのアイコンを取得するには**
  
1. [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md)メソッドを呼び出して[、IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)インターフェイスへのポインターを取得します。 
    
2. [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)メソッドを呼び出して[、IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)インターフェイスへのポインターを取得します。 
    
3. アイコン ハンドル [を取得するには、IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) メソッドを呼び出します。 
    
このアイコンは、標準の Win32 API を使用して表示できます。
  
> [!IMPORTANT]
> メッセージ クラスのアイコンを取得したら、そのアイコンをキャッシュするためにあらゆる努力をします。 アイコンをキャッシュしないは、クライアント アプリケーションのパフォーマンスに重大な影響を与えます。 アイコンをキャッシュする場合は、メッセージ クラスとそのサブクラス間の関係に注意してください。 たとえば、IPM の場合です。メモ.Meeting.Cancel メッセージ クラスは IPM に解決されます。注: IPM のすべてのサブクラスを想定していない。メモでは、IPM のアイコンを使用する必要があります。注。 
  

