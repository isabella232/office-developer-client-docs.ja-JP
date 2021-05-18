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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316311"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>PidTagFolderWebViewInfo 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft のフォルダーのホーム ページの URL が含Outlook。 このプロパティには **、WebViewPersistenceObject というバイナリ ストリームが含まれます**。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|識別子:  <br/> |0x36DF  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI フォルダー  <br/> |
   
## <a name="remarks"></a>注釈

ホーム ページの URL は、任意のフォルダーにOutlookできます。 この情報は、フォルダー Outlook [プロパティ] ダイアログ ボックスの **[** ホーム ページ] タブからアクセスできます。 
  
特定のポリシー設定によっては、このフォルダーを含む MAPI ストアが[IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md)実装で MSCAP_SECURE_FOLDER_HOMEPAGES を報告しない場合、ホーム ページは Outlook によって無視される場合があります。 
  
[今日 **Outlook]フォルダー** とパブリック フォルダーの両方に、ホーム ページの URL を設定できます。 ただし **、Outlook Today** フォルダーは、別のメカニズムを使用してホーム ページの URL を管理します。このメカニズムについては、このトピックでは説明しない。 パブリック フォルダーには、ユーザーに固有のホーム ページ URL が定義されている場合があります。 ただし、この機能については、このトピックでは説明していない。 
  
このプロパティの値は **、WebViewPersistenceObject というバイナリ ストリームです**。
  
### <a name="webviewpersistenceobject-stream-structure"></a>WebViewPersistenceObject ストリーム構造

**WebViewPersistenceObject ストリーム** 構造には、フォルダーのホーム ページ URL に関する情報が含まれます。 
  
この構造体のデータ要素は、次の指定された順序で、お客様の直後に、リトル エンドのバイト順に格納されます。 
  
> [!NOTE]
> 次の説明では、ユーザーがサポートするフィールド値の一覧Outlook。したがって、コードが既存のストリームを読み取る場合、ここにリストされていないフラグも見つかる可能性があります。 ただし、この説明を使用すると、プログラムで理解できる **PidTagFolderWebViewInfo** プロパティOutlook作成できます。 
  
 _dwVersion_
  
> DWORD (4 バイト)。 構造の形式のバージョン。 2007 Microsoft Office Outlook現在、このフィールドでサポートされている唯一の値は次のとおりです。
    
|**値の名前**|**値**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 バイト)。 ホーム ページ情報の種類。 2007 Microsoft Office Outlook現在、このフィールドでサポートされている唯一の値は次のとおりです。
    
|**値の名前**|**値**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 バイト)。 次の表に、値と意味を持つ 0 個以上のフラグの組み合わせ。
    
|フラグ名****|****値****|****説明****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |[**このフォルダーのホーム ページ** を既定で表示する] チェックボックスは、フォルダーの [プロパティ] ダイアログ ボックスの [ホーム ページ] タブでオンになっています。  <br/> |
   
 _dwUnused[7]_
  
> 7 DWORD 要素の配列 (合計 28 バイト)。 未使用。
    
cbData
  
> ULONG (4 バイト)。 _wzURL_ データ要素のサイズ (バイト単位)。 
    
 _wzURL_
  
> WCHAR 要素の配列。 終了ゼロのホーム ページ URL 文字列の UTF-16 表記。
    
### <a name="webviewpersistenceobject-stream-sample"></a>WebViewPersistenceObject ストリームのサンプル

このセクションでは **、WebViewPersistenceObject ストリームの例について説明** します。 ストリームは、ホーム ページの URL " を指定 https://www.microsoft.com します。 
  
 **データ ダンプ**
  
バイナリ エディターに表示されるストリームのデータ ダンプを次に示します。
  
|**ストリーム のオフセット**|**データ バイト**|**ASCII データ**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
**WebViewPersistenceObject** ストリームのサンプル データの解析を次に示します。 
  
 _dwVersion_
  
> オフセット0x0 4 バイト: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION)。
    
 _dwType_
  
> オフセット0x4 4 バイト: 0x00000001 (WEBVIEWURL)。
    
 _dwFlags_
  
> オフセット0x8 4 バイト: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT)。
    
 _dwUnused[7]_
  
> オフセット0xC 28 バイト: すべてのゼロ。
    
 _cbData_
  
> オフセット0x28、4 バイト: 0x00000032。
    
 _wzURL_
  
> オフセット0x2C、0x32バイト: 25 WCHARs の配列。 Unicode のゼロ終端文字列値: " https://www.microsoft.com ".
    

