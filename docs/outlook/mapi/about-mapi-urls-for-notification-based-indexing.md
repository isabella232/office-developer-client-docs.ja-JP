---
title: インデックス作成の MAPI URL Notification-Basedについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: '最終更新日: 2011 年 11 月 08 日'
ms.openlocfilehash: 5a3e45809f36b71968560a4b239e268addf00474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422482"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>インデックス作成の MAPI URL Notification-Basedについて

**適用対象**: Outlook 2013 | Outlook 2016 
  
ストア プロバイダーは、インデクサーにオブジェクトのインデックス作成の準備ができていることを通知すると、MAPI プロトコル ハンドラーに対してオブジェクトを一意に識別する MAPI URL を生成します。 MAPI URL は Unicode でエンコードされ、次の形式になります。 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

次の表では、一般的な URL のさまざまな部分について説明します。

|指定項目 | 説明|
|:----|:-----------|  
|*SID* |現在のユーザーのセキュリティ識別子。| 
|*StoreDisplayName* |そのストア上のユーザーの表示名を指定する文字列。|
|*HashNumber* |ストア エントリ ID またはストア マッピング署名に基づいて計算される 16 進表記の **DWORD。** この値はレジストリに格納され、後で MAPI プロトコル ハンドラーのストアを識別するために使用されます。<br/><br/>この数値は、他のストアとの競合を最小限に抑える方法で計算する必要があります。 Microsoft がハッシュ番号の計算Outlook使用するアルゴリズムについては[、「Algorithm to Calculate the Store Hash Number」を参照してください](algorithm-to-calculate-the-store-hash-number.md)。|
|*StoreType* |インデックスを作成するオブジェクトを含むストアの種類を識別する番号。 次の値が示される可能性があります。<br/>- 0 - 既定のストア。<br/><br/>- 1 - ローカルにキャッシュされたデリゲート アイテムに使用されるデリゲート ストア。<br/><br/>- 2 - パブリック フォルダー、パブリック フォルダーのお気に入りに使用します。<br/><br/>**メモ**: ストアがプッシュではなくクロールされている場合、使用される値は文字 *X です*。| 
|*FolderNameA/.../FolderNameN* |フォルダーのルートからのパスIPM_SUBTREEメッセージに移動します。 たとえば、[受信トレイ] の [ファミリ] **フォルダー内** の **メッセージには、** この **パラメーターの受信トレイ/ファミリ** があります。 |
|*EntryIDEncoded* |Unicode 文字列としてエンコードされたアイテムの MAPI エントリ ID。 特定の特殊文字のエンコード方法については、以下の「特殊文字」を参照してください。 エントリ ID をエンコードするアルゴリズムの詳細については、「Algorithm to Encode Entry IDs and [Attachment ID」を参照してください](algorithm-to-encode-entry-ids-and-attachment-ids.md)。<br/><br/>**メモ**: テキストとして表示される場合、このエンコードされたエントリ ID は、使用可能なフォントに応じて、アルゴリズムに準拠してランダムなハングル文字またはボックスとして表示されます。  |
|*AttachIDEncoded* |Unicode 文字列としてエンコードされた添付ファイル ID。 特定の特殊文字のエンコード方法については、以下の「特殊文字」を参照してください。 エントリ ID をエンコードするアルゴリズムの詳細については、「Algorithm to Encode Entry IDs and [Attachment ID」を参照してください](algorithm-to-encode-entry-ids-and-attachment-ids.md)。<br/><br/>**メモ**: テキストとして表示される場合、このエンコードされたエントリ ID は、使用可能なフォントに応じて、アルゴリズムに準拠してランダムなハングル文字またはボックスとして表示されます。 |
|*FileName* |メッセージに表示される添付ファイルの名前。|
    
## <a name="examples-of-mapi-urls"></a>MAPI URL の例

MAPI URL の例を次に示します。
  
- フォルダーの MAPI URL: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- メッセージの MAPI URL: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- 添付ファイルの MAPI URL: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>特殊文字

メッセージまたは添付ファイルに表示される場合、特定の文字がエンコードされます。 MAPI URL でエンコードされる文字を次に示します。
  
- % > %25
    
- / > %2F 
    
- \ > %5C 
    
- \* > %2A 
    
- ? > %3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>各 MAPI URL に関連付けられた BLOB

インデックスを作成するオブジェクトの MAPI URL をプッシュすると、ストア プロバイダーは MAPI プロトコル ハンドラーの特定の情報を含むバイナリ ラージ オブジェクト (BLOB) も作成します。 ストア プロバイダーは、この BLOB を各 MAPI URL に関連付け、MAPI URL をインデクサーにプッシュするときに送信します。 BLOB の形式は次のとおりです。 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

ストア プロバイダーは、これらの値を示す順序で BLOB に書き込む必要があります。 次の表では、BLOB の各フィールドについて説明します。

|指定項目 | 説明|
|:----|:-----------|  
|*dwVersion* |これは、送信されるデータのバージョンです。 現在、この値は 1 です。|
|*dwFlags* |将来使用するために予約されています。 現在、この値は 0 である必要があります。|
|*cbProfileName* |プロファイル名のサイズ (バイト単位)。 この情報は、MAPI プロトコル ハンドラーがアイテムのインデックス作成時に使用するプロファイルを知る際に役立ちます。|
|*wszProfileName* |プロファイル名を含む Null 終端 Unicode 文字列。|
|*cbProviderItemID* |プロバイダー アイテム ID のサイズ (バイト単位)。 ストア プロバイダーは、この情報を取得するために追加のフォルダーを開かねないで、フォルダーのプロバイダー アイテム ID のみを送信する必要があります。|
|*wszProviderItemID* |ストア内のアイテムを一意に識別するプロバイダー アイテム ID を持つ Null で終了する Unicode 文字列。|
    
## <a name="see-also"></a>関連項目

- [ストア インデックスNotification-Basedについて](about-notification-based-store-indexing.md)
- [MAPI 定数](mapi-constants.md)

