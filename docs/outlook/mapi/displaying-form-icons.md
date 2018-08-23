---
title: フォーム アイコンの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b2e79e5568de38bee9a97c9df2598b30f1ba1bdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799940"
---
# <a name="displaying-form-icons"></a>フォーム アイコンの表示

  
  
**適用対象**: Outlook 
  
、フォルダー内のメッセージの一覧を表示するとき、ユーザーに役に立つ場合は標準の IPM とカスタム メッセージ クラスを持つメッセージを区別します。メッセージに注意してください。 カスタム メッセージ クラスは、フォームのサーバーに対応し、フォーム サーバーが自身を表すアイコンを提供します。 ユーザーがメッセージを開く前に、各メッセージのメッセージ クラスにユーザーに警告するメッセージの一覧にこれらのアイコンを表示できます。 通常、フォームの**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) のプロパティのアイコンは、メッセージの一覧に表示する必要があります。 フォームには、プロパティ シートでフォームが最小化したときに表示できる**PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティが設定されています。
  
 **そのメッセージ クラスのフォームのサーバーをアクティブにすることがなく、メッセージ クラスのアイコンを取得するには**
  
1. ポインターを取得する[IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md)メソッドを呼び出して、 [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md)インタ フェースです。 
    
2. ポインターを取得する[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)メソッドを呼び出して、 [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)インタ フェースです。 
    
3. アイコンのハンドルを取得する[IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md)メソッドを呼び出します。 
    
標準の Win32 Api を使用してアイコンを表示し、ことができます。
  
> [!IMPORTANT]
> メッセージ クラスのアイコンがある場合は、そのアイコンをキャッシュするよう努力することです。 クライアント アプリケーションのパフォーマンスに影響を与える深刻なアイコンをキャッシュしません。 アイコンをキャッシュする場合は、メッセージ クラスとそのサブクラスの関係の注意します。 などの場合は、IPM。Note.Meeting.Cancel メッセージ クラスは IPM に解決するために発生します。注意してくださいと仮定しないでをすべて IPM のサブクラスです。注記では、IPM のアイコンを使用する必要があります。注意してください。 
  

