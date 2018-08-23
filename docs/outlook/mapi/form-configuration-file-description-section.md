---
title: フォーム構成ファイル [Description] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8ad5fd9cf437afc3999697792850548e4e5a1435
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582897"
---
# <a name="form-configuration-file-description-section"></a>フォーム構成ファイル [Description] セクション
 
**適用されます**: Outlook 2013 |Outlook 2016 
  
**[説明]** セクションには、フォームのコントロールでは、[フォームのユーザー インターフェイスでは、フォームの検索に使用される属性に関連付けられているすべてのプロパティが一覧表示されます。 **MessageClass**、 **Clsid**、および**表示名**のエントリは、フォームのメッセージ クラス、その GUID、およびメッセージ クラスの表示名の名前をそれぞれ識別するには、フォーム ライブラリ内でフォームを検索するため、必要なエントリをします。. 残りのエントリはオプションです。 **[説明]** セクションの形式は次のとおりです。 
  
**[説明]** セクションには、フォームのコントロールでは、[フォームのユーザー インターフェイスでは、フォームの検索に使用される属性に関連付けられているすべてのプロパティが一覧表示されます。 **MessageClass**、 **Clsid**、および**表示名**のエントリは、フォームのメッセージ クラス、その GUID、およびメッセージ クラスの表示名の名前をそれぞれ識別するには、フォーム ライブラリ内でフォームを検索するため、必要なエントリをします。. 残りのエントリはオプションです。 **[説明]** セクションの形式は次のとおりです。 
  
 **[説明]MessageClass** =  _の文字列_
  
 **Clsid** =  _guid_
  
 **表示名** =  _displayedstring_
  
 **SmallIcon** =  _のパス_
  
 **LargeIcon** =  _のパス_
  
省略可能なエントリは次のとおりです。
  
 **カテゴリ** =  _の文字列が表示されます_
  
 **サブカテゴリ** =  _の文字列が表示されます_
  
 **コメント** =  _の文字列が表示されます_
  
 **所有者** =  _の文字列が表示されます_
  
 **数** =  _の文字列が表示されます_
  
 **バージョン** =  _の整数_
  
 **ロケール** =  _の文字列_
  
 **非表示** =  _の整数_
  
 **DesignerToolName** =  _の文字列_
  
 **DesignerToolGuid** =  _clsid_
  
 **DesignerRuntimeGuid** =  _clsid_
  
 **ComposeInFolder** =  _0 | 1_
  
 **ComposeCommand** =  _の文字列_
  
**カテゴリ**と**サブカテゴリ**のエントリは、クライアント アプリケーションのユーザー インターフェイス内のフォームの既定の分類を設定するのには、フォームのインストーラーによって使用されます。 などの階層が設定するカテゴリの「ヘルプデスク」のある、「ソフトウェア」および「ハードウェア」サブカテゴリ。 この分類より整理された形でメッセージを表示するビューアーのアプリケーションで使用できます。 **コメント**、**所有者**、および**番号**のエントリは、クライアント アプリケーションのユーザー インターフェイスに表示されるすべてのコメント文字列です。 これらは、フォームの開発者の裁量で使用できるフォーム固有のプロパティです。 たとえば、フォーム、人や、フォームの管理を担当する組織を指定するための**所有者**のエントリと、フォームの別のバージョンを追跡するための番号の目的を示すために**コメント**の入力を使用できます。 **コメント**のコメントの 10 行までのエントリを含めることできます。 コメントの最初の行では、「コメント」という単語を使用して、キーとして、コメントの 2 行目が"Comment9"にしますを通じてというようにキーとして"Comment1"を使用して 
  
**LargeIcon** 、 **SmallIcon**エントリ アイコンを表示するクライアント アプリケーションのユーザー インターフェイスで使用されるアイコン リソースへのパスを指定するため、通常これは、 **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) を含むテーブルの行または**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) のプロパティの列を選択します。 アイコンのファイル名は、フォーム構成ファイルがインストールされているディレクトリからの相対パス名として指定できます。 **バージョン**エントリを使用して、フォームのバージョン番号を指定します。 **ロケール**は、移動先のフォーム ライブラリの 3 文字の言語識別子です。 これらの識別子の一覧については、 _Win32 プログラマーズ リファレンス_を参照しています。
  
**隠し**エントリは、フォームをフォーム ライブラリ プロバイダーのユーザー インターフェイスに表示かどうかを示します: 1 ことを示し、ファイルが隠しファイル 0 は、フォームが表示されていることを示します。 次のフォーム構成ファイルの例が表示されます。 
  
**ComposeInFolder**エントリは、フォームにユーザーがそれを作成するときにメッセージを保存すると、現在のフォルダーまたはユーザーの受信トレイに配置するよう設計されて かどうかを制御: 1 ことを示し、フォームが現在のフォルダーに移動する必要があります必要がある場合は 0受信トレイに移動します。 
  
**ComposeCommand**エントリは、クライアント アプリケーションに格納する文字列は、メニューを作成のです。 これを指定しない場合は、**表示名**のエントリが使用されます。 
  
```cpp
[Description]
MessageClass = IPM.Help
Clsid = {00020D31-0000-0000-C000-000000000046}
DisplayName = Help Desk Request Form
;optional entries
Category = Help Desk Requests
Subcategory = New Requests
Comment = Use this form to request network assistance
Owner = Help Desk
Number = 1
SmallIcon = C:\WINDOWS|EFORMS\HELPDESK\HDSMALL.ICO
LargeIcon = C:\WINDOWS|EFORMS\HELPDESK\HDLARGE.ICO
Version = 1.00
Locale = enu
Hidden = 0
ComposeInFolder = 0
ComposeCommand = &Help Desk Request
 
```


