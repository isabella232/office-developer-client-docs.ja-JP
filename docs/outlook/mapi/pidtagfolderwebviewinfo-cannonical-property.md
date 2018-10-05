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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389961"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>PidTagFolderWebViewInfo 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook でフォルダーのホーム ページの URL が含まれています。 このプロパティには、 **WebViewPersistenceObject**と呼ばれるバイナリ ストリームが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|識別子:  <br/> |0x36DF  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI フォルダー  <br/> |
   
## <a name="remarks"></a>備考

すべての Outlook フォルダーのホーム ページの URL を指定できます。 この情報は、Outlook のフォルダーの [プロパティ] ダイアログ ボックスの [**ホーム ページ**] タブからアクセスできます。 
  
特定のポリシー設定によっては、 [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md)実装では、このフォルダーが格納されている MAPI ストアに MSCAP_SECURE_FOLDER_HOMEPAGES が報告されない場合、Outlook でホーム ページを無視して可能性がありますされます。 
  
**Outlook Today** ] フォルダーとパブリック フォルダーの両方には、ホーム ページの Url を持つことができます。 ただし**Outlook** today メカニズムを使用して、さまざまな管理のホーム ページの URL です。そのメカニズムは、このトピックでは説明しません。 パブリック フォルダーで定義されているホーム ページの URL、ユーザーに固有であるともあります。 ただし、その機能は、このトピックでは説明しません。 
  
このプロパティの値は、 **WebViewPersistenceObject**と呼ばれるバイナリ ストリームです。
  
### <a name="webviewpersistenceobject-stream-structure"></a>WebViewPersistenceObject ストリームの構造

**WebViewPersistenceObject**ストリームの構造体には、フォルダーのホーム ページの URL に関する情報が含まれています。 
  
この構造内のデータ要素は、次の指定された順序で 1 つ別のすぐ後、リトル エンディアンのバイト順で格納されます。 
  
> [!NOTE]
> 次の説明が表示されていないすべての Outlook でサポートされているフィールド値したがって、コードは、既存のストリームを読み取る、ときにここに記載されていないいくつかのフラグもみられます。 ただし、この説明を使用すると、Outlook を理解する**PidTagFolderWebViewInfo**プロパティの値をプログラムで作成します。 
  
 _dwVersion_
  
> DWORD (4 バイト)。 構造体の形式のバージョンです。 Microsoft Office Outlook 2007 では、現在このフィールドに対してのみサポートされている値はとおりです。
    
|**値の名前**|**値**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 バイト)。 ホーム ページの情報の種類です。 Microsoft Office Outlook 2007 では、現在このフィールドに対してのみサポートされている値はとおりです。
    
|**値の名前**|**値**|
|:-----|:-----|
|いる  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 バイト)。 フラグの値を 0 個以上の組み合わせと意味は次の表に記載されています。
    
|フラグの名前。|****値****|****説明****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |**このフォルダーの既定のホーム ページを表示**] チェック ボックスは、フォルダーの [プロパティ] ダイアログ ボックスの [**ホーム ページ**] タブにチェックインされました。  <br/> |
   
 _dwUnused [7]_
  
> 7 つの DWORD の要素 (28 バイトの合計) の配列です。 未使用。
    
cbData
  
> ULONG (4 バイト) です。 _WzURL_データ要素のバイト単位のサイズです。 
    
 _wzURL_
  
> WCHAR 要素の配列。 ホーム ページの 0 で終わる URL 文字列の utf-16 表現。
    
### <a name="webviewpersistenceobject-stream-sample"></a>WebViewPersistenceObject ストリームのサンプル

このセクションでは、 **WebViewPersistenceObject**ストリームの例について説明します。 ストリーム ホーム ページの URL を指定する"https://www.microsoft.com"です。 
  
 **データのダンプ**
  
次のストリームのデータのダンプがバイナリ エディターで表示します。
  
|**ストリームのオフセット**|**データのバイト数**|**ASCII データ**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
**WebViewPersistenceObject**ストリームのサンプル データの解析は、次のようにします。 
  
 _dwVersion_
  
> 0x0 では、4 バイトのオフセット: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION)。
    
 _dwType_
  
> 0x4、4 バイトのオフセット: 0x00000001 (いる)。
    
 _dwFlags_
  
> 0x8、4 バイトのオフセット: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT)。
    
 _dwUnused [7]_
  
> 0 xc、28 バイトのオフセット: すべてゼロです。
    
 _cbData_
  
> 4 バイト目の 0x28 にオフセット: 0x00000032。
    
 _wzURL_
  
> オフセット 0x2C、0x32 バイト: 25 WCHARs の配列です。 Unicode 0 で終わる文字列の値:"https://www.microsoft.com"です。
    

