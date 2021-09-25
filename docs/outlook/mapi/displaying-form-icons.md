---
title: フォーム アイコンの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2b7177c72d1d60d75c64bfaaf5e85fba46c4aa3d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551680"
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
  

