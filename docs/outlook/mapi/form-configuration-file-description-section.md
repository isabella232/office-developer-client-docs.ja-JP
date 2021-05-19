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
  
**[説明] セクションには**、フォームのユーザー インターフェイスのコントロールに関連付けられているフォームのすべてのプロパティと、フォームの検索に使用される属性が一覧表示されます。 フォーム のメッセージ クラスの名前、GUID、およびメッセージ クラスの表示名をそれぞれ識別する MessageClass、Clsid、**および DisplayName** エントリは、フォーム ライブラリ内でフォームを検索するために使用される必須エントリです。   残りのエントリはオプションです。 [説明] セクション **の形式は** 次の形式です。 
  
**[説明] セクションには**、フォームのユーザー インターフェイスのコントロールに関連付けられているフォームのすべてのプロパティと、フォームの検索に使用される属性が一覧表示されます。 フォーム のメッセージ クラスの名前、GUID、およびメッセージ クラスの表示名をそれぞれ識別する MessageClass、Clsid、**および DisplayName** エントリは、フォーム ライブラリ内でフォームを検索するために使用される必須エントリです。   残りのエントリはオプションです。 [説明] セクション **の形式は** 次の形式です。 
  
 **[説明] MessageClass**  =  _string_
  
 **Clsid**  =  _guid_
  
 **DisplayName**  =  _displayedstring_
  
 **SmallIcon**  =  _path_
  
 **LargeIcon**  =  _path_
  
オプションのエントリは次のとおりです。
  
 **カテゴリ**  =  _表示される文字列_
  
 **Subcategory**  =  _表示される文字列_
  
 **コメント**  =  _表示される文字列_
  
 **所有者**  =  _表示される文字列_
  
 **数値**  =  _表示される文字列_
  
 **バージョン**  =  _integer_
  
 **ロケール**  =  _string_
  
 **非表示**  =  _integer_
  
 **DesignerToolName**  =  _string_
  
 **DesignerToolGuid**  =  _clsid_
  
 **DesignerRuntimeGuid**  =  _clsid_
  
 **ComposeInFolder**  =  _0|1_
  
 **ComposeCommand**  =  _string_
  
Category **エントリ** と **Subcategory エントリ** は、フォーム インストーラーによって使用され、クライアント アプリケーションのユーザー インターフェイス内でフォームの既定の分類を設定します。 たとえば、"Help Desk" がカテゴリで、"Software" と "Hardware" がサブカテゴリである階層を設定できます。 この分類は、ビューアー アプリケーションによって、より整理された方法でメッセージを表示するために使用できます。 コメント **、****所有者、および****番号** のエントリは、クライアント アプリケーションのユーザー インターフェイスに表示されるコメント文字列です。 これらは、フォーム開発者の裁量で使用できるフォーム固有のプロパティです。 たとえば、コメントエントリを使用して、フォームの目的、フォームの管理を担当する人物または組織を示すために使用される所有者エントリ、およびフォームの異なるバージョンを追跡するために使用される番号を示します。 コメント エントリ **には** 、最大 10 行のコメントを含めできます。 コメントの最初の行では、キーとして "Comment" という単語を使用し、2 行目のコメントでは "Comment1" をキーとして使用し、"Comment9" を使用します。 
  
**LargeIcon** および **SmallIcon** エントリは、クライアント アプリケーションのユーザー インターフェイスにアイコンを表示するために使用されるアイコン リソースのパスを指定するために使用されます。通常、これは PR_ICON ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティ列または PR_MINI_ICON (  [PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティ列を含むテーブル行の場合です。  アイコン ファイル名は、フォーム構成ファイルがインストールされているディレクトリを基準にパス名として指定できます。 Version **エントリ** は、フォームのバージョン番号を示すために使用されます。 **Locale** は、移動先フォーム ライブラリの 3 文字の言語識別子です。 これらの識別子の一覧は  _、「Win32 プログラマリファレンス」を参照してください_。
  
[ **非表示** ] エントリは、フォームをフォーム ライブラリ プロバイダーのユーザー インターフェイスに表示するかどうかを示します。1 はファイルが非表示で、0 はフォームが表示されているかどうかを示します。 フォーム構成ファイルの例を次に示します。 
  
**ComposeInFolder** エントリは、ユーザーがメッセージを作成中に保存するときに、フォームを現在のフォルダーまたはユーザーの受信トレイに配置するように設計されているかどうかを制御します。1 は、フォームが現在のフォルダーに移動することを示し、0 は受信トレイに移動することを示します。 
  
**ComposeCommand** エントリは、クライアント アプリケーションの作成メニューに配置される文字列です。 これを指定しない場合は **、DisplayName** エントリが使用されます。 
  
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


