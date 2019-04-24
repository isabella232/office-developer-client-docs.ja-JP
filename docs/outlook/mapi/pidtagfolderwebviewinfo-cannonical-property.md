---
title: PidTagFolderWebViewInfo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316311"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>PidTagFolderWebViewInfo 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook のフォルダーのホームページの URL が保存されています。 このプロパティには、 **WebViewPersistenceObject**と呼ばれるバイナリストリームが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|識別子:  <br/> |0x36DF  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI フォルダー  <br/> |
   
## <a name="remarks"></a>解説

ホームページの URL は任意の Outlook フォルダーに指定できます。 この情報には、Outlook でフォルダーの [プロパティ] ダイアログボックスの [**ホームページ**] タブからアクセスできます。 
  
特定のポリシー設定によっては、ホームページが Outlook で無視されることがあります。このフォルダーを含む MAPI ストアでは、 [imscapabilities:: getcapabilities](pidtagfolderwebviewinfo-cannonical-property.md)実装の MSCAP_SECURE_FOLDER_HOMEPAGES が報告されない場合があります。 
  
**Outlook Today**フォルダーとパブリックフォルダーの両方に、ホームページの url を設定できます。 ただし、 **Outlook Today**フォルダーでは、ホームページの URL を管理するために別のメカニズムを使用しています。このトピックでは、このメカニズムについては説明しません。 パブリックフォルダーには、ユーザーに固有のホームページの URL が定義されている場合もあります。 ただし、このトピックではこの機能については説明しません。 
  
このプロパティの値は、 **WebViewPersistenceObject**と呼ばれるバイナリストリームです。
  
### <a name="webviewpersistenceobject-stream-structure"></a>WebViewPersistenceObject Stream 構造

**WebViewPersistenceObject** stream 構造には、フォルダーのホームページの URL に関する情報が含まれています。 
  
この構造体の Data 要素は、次の指定された順序で、すぐに、リトルエンディアンバイト順に格納されます。 
  
> [!NOTE]
> 次の説明では、Outlook でサポートされているすべてのフィールド値が一覧表示されない場合があります。そのため、コードで既存のストリームを読み取る場合、ここに記載されていないフラグも検索されることがあります。 ただし、この説明を使用して、Outlook が認識する**PidTagFolderWebViewInfo**プロパティの値をプログラムで作成することができます。 
  
 _dwversion_
  
> DWORD (4 バイト)。 構造体の形式のバージョン。 Microsoft Office Outlook 2007 の場合、このフィールドでサポートされている値は次のとおりです。
    
|**値の名前**|**値**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 バイト)。 ホームページ情報の種類を示します。 Microsoft Office Outlook 2007 の場合、このフィールドでサポートされている値は次のとおりです。
    
|**値の名前**|**値**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 バイト)。 次の表に、値と意味を含む0個以上のフラグの組み合わせを示します。
    
|フラグ名 * * * *|****値****|****説明****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |フォルダーの [プロパティ] ダイアログボックスの [**ホームページ**] タブで、[**このフォルダーに既定でホームページを表示**する] チェックボックスがオンになっています。  <br/> |
   
 _dwunused [7]_
  
> 7個の DWORD 要素の配列 (合計28バイト)。 使用.
    
cbdata
  
> ULONG (4 バイト)。 _wzURL_ data 要素のサイズ (バイト単位)。 
    
 _wzURL_
  
> WCHAR 要素の配列。 0で終了したホームページの URL 文字列の utf-16 表現。
    
### <a name="webviewpersistenceobject-stream-sample"></a>WebViewPersistenceObject Stream サンプル

このセクションでは、 **WebViewPersistenceObject**ストリームの例について説明します。 ストリームは、ホームページの URL "https://www.microsoft.com" を指定します。 
  
 **データダンプ**
  
次に示すのは、バイナリエディターに表示されるストリームのデータダンプです。
  
|**ストリームオフセット**|**データバイト**|**ASCII データ**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
以下に、 **WebViewPersistenceObject**ストリームのサンプルデータの解析を示します。 
  
 _dwversion_
  
> Offset 0x0、4バイト: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION)。
    
 _dwType_
  
> オフセット0x4、4バイト: 0x00000001 (webviewurl)。
    
 _dwFlags_
  
> オフセット0x8、4バイト: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT)。
    
 _dwunused [7]_
  
> Offset 0xC, 28 バイト: すべて0。
    
 _cbdata_
  
> オフセット0x28、4バイト: 0x00000032。
    
 _wzURL_
  
> Offset 0x2C、0x32 バイト:25 wchars の配列。 Unicode の0で終わる文字列値: "https://www.microsoft.com"。
    

