---
title: フォーム構成ファイル [説明] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433095"
---
# <a name="form-configuration-file-description-section"></a>フォーム構成ファイル [説明] セクション
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
**[Description]** セクションには、フォームのユーザーインターフェイスのコントロールに関連付けられているフォームのすべてのプロパティと、フォームの場所を特定するために使用される属性が表示されます。 フォームのメッセージクラスの名前、GUID、およびメッセージクラスの表示名を識別する**messageclass**、 **Clsid**、 **DisplayName**の各エントリは、フォームライブラリ内でフォームを検索するために使用される必須のエントリです。. 残りのエントリは省略可能です。 **[Description]** セクションの形式は次のとおりです。 
  
**[Description]** セクションには、フォームのユーザーインターフェイスのコントロールに関連付けられているフォームのすべてのプロパティと、フォームの場所を特定するために使用される属性が表示されます。 フォームのメッセージクラスの名前、GUID、およびメッセージクラスの表示名を識別する**messageclass**、 **Clsid**、 **DisplayName**の各エントリは、フォームライブラリ内でフォームを検索するために使用される必須のエントリです。. 残りのエントリは省略可能です。 **[Description]** セクションの形式は次のとおりです。 
  
 **Descriptionmessageclass** =  _文字列_
  
 **Clsid** =  _guid_
  
 **DisplayName** =  表示_文字列_
  
 **SmallIcon** =  _パス_
  
 **LargeIcon** =  _パス_
  
省略可能なエントリは次のとおりです。
  
 **カテゴリ** =  で_表示される文字列_
  
 **サブカテゴリ** =  で_表示される文字列_
  
 **コメント** =  の_表示文字列_
  
 **所有者** =  が表示した_文字列_
  
 **数値** =  で_表示される文字列_
  
 **バージョン** =  _整数_
  
 **ロケール** =  _文字列_
  
 **非表示** =  の_整数_
  
 **DesignerToolName** =  _文字列_
  
 **デザイナツール guid** =  _clsid_
  
 **designerrアン timeguid** =  _clsid_
  
 **構成ファイル** =  _0 | 1_
  
 **ComposeCommand** =  _文字列_
  
**カテゴリ**および**サブカテゴリ**のエントリは、フォームインストーラーによって使用され、クライアントアプリケーションのユーザーインターフェイス内のフォームの既定の分類を設定します。 たとえば、"Help Desk" がカテゴリで、"ソフトウェア" と "ハードウェア" がサブカテゴリである階層を設定することができます。 この分類は、ビューアーアプリケーションで、より整理された方法でメッセージを表示するために使用できます。 **コメント**、**所有者**、および**番号**エントリは、クライアントアプリケーションのユーザーインターフェイスに表示されるすべてのコメント文字列です。 フォーム開発者の裁量で使用できるフォーム固有のプロパティです。 たとえば、**コメント**エントリを使用して、フォームの目的、フォームの管理を担当する個人または組織の指定に使用する**所有者**エントリ、およびフォームの異なるバージョンの追跡に使用される番号を示すことができます。 **コメント**エントリでは、最大10行のコメントを含めることができます。 コメントの最初の行では、キーとして "Comment" という単語を使用し、2番目のコメントでは "Comment1" をキーとして使用し、次に "Comment9" を使用します。 
  
**LargeIcon**および**SmallIcon**エントリは、クライアントアプリケーションのユーザーインターフェイスにアイコンを表示するために使用されるアイコンリソースのパスを指定するために使用されます。通常、これは、 **PR_ICON**を含むテーブル行用です ([PidTagIcon](pidtagicon-canonical-property.md))。or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティの列。 アイコンファイル名は、フォーム構成ファイルがインストールされているディレクトリを基準としたパス名として指定できます。 **バージョン**エントリは、フォームのバージョン番号を示すために使用されます。 **ロケール**は、送信先フォームライブラリの3文字の言語識別子です。 これらの識別子の一覧については、 _Win32 プログラマーズリファレンスを参照_してください。
  
**非表示**のエントリは、フォームをフォームライブラリプロバイダのユーザーインターフェイスに表示するかどうかを示します。1は、ファイルが非表示になっていることを示し、0は、フォームが表示されていることを示します。 フォーム構成ファイルの例を次に示します。 
  
構成**** するには、次のようにします。1は、ユーザーがメッセージを作成中に保存するときに、現在のフォルダーまたはユーザーの受信トレイにフォームを配置するように設計されているかどうかを制御します。1は、フォームが現在のフォルダーに移動することを示し、0は受信トレイに移動します。 
  
**ComposeCommand** entry は、クライアントアプリケーションの [新規作成] メニューに配置される文字列です。 この引数を指定しない場合は、 **DisplayName**エントリが使用されます。 
  
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


