---
title: 通知ベースのインデックス作成の MAPI url について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: '最終更新日: 2011 年11月8日'
ms.openlocfilehash: 5a3e45809f36b71968560a4b239e268addf00474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422482"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>通知ベースのインデックス作成の MAPI url について

**適用対象**: Outlook 2013 | Outlook 2016 
  
ストアプロバイダーは、オブジェクトがインデックス処理の準備が整っていることをインデクサーに通知すると、mapi プロトコルハンドラーにオブジェクトを一意に識別する mapi URL を生成します。 MAPI url は Unicode でエンコードされ、次の形式になります。 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

次の表に、一般的な URL のさまざまな部分を示します。

|パーツ | 説明|
|:----|:-----------|  
|*SID* |現在のユーザーのセキュリティ識別子。| 
|*storedisplayname* |そのストア上のユーザーの表示名を指定する文字列。|
|*hashnumber* |ストアエントリ ID またはストアマッピングシグネチャに基づいて計算される16進表記の**DWORD** 。 この値は、レジストリに格納され、後で MAPI プロトコルハンドラーでストアを識別するために使用されます。<br/><br/>この数値は、他のストアとの競合を最小限に抑えるように計算する必要があります。 Microsoft Outlook がハッシュ番号を計算するために使用するアルゴリズムについては、「 [Store ハッシュ番号を計算するアルゴリズム](algorithm-to-calculate-the-store-hash-number.md)」を参照してください。|
|*StoreType* |インデックスを作成するオブジェクトが格納されているストアの種類を識別する番号。 次の値が示される可能性があります。<br/>-0-既定のストア。<br/><br/>-1-ローカルにキャッシュされた代理人のアイテムに使用される代理人ストア。<br/><br/>-2-パブリックフォルダーのお気に入りに使用されます。<br/><br/>**注**: ストアがプッシュされる代わりにクロールされる場合、使用される値は文字*X*です。| 
|*foldernamea/.../foldernamea* |フォルダーまたはメッセージへの IPM_SUBTREE のルートからのパス。 たとえば、**受信トレイ**の下にある [**家族**] フォルダー内のメッセージには、このパラメーターの**inbox/Family**があります。 |
|*entryidencoded* |Unicode 文字列としてエンコードされたアイテムの MAPI エントリ ID。 特定の特殊文字がどのようにエンコードされるかについては、以下の「特殊文字」を参照してください。 エントリ id をエンコードするアルゴリズムの詳細については、「 [entry id とアタッチメント id をエンコードするためのアルゴリズム](algorithm-to-encode-entry-ids-and-attachment-ids.md)」を参照してください。<br/><br/>**注**: テキストとして表示される場合、このエンコードされたエントリ ID は、使用可能なフォントによっては、アルゴリズムに準拠して、ハングル文字またはボックスがランダムに表示されます。  |
|*attachidencoded* |Unicode 文字列としてエンコードされた添付ファイル ID。 特定の特殊文字がどのようにエンコードされるかについては、以下の「特殊文字」を参照してください。 エントリ id をエンコードするアルゴリズムの詳細については、「 [entry id とアタッチメント id をエンコードするためのアルゴリズム](algorithm-to-encode-entry-ids-and-attachment-ids.md)」を参照してください。<br/><br/>**注**: テキストとして表示される場合、このエンコードされたエントリ ID は、使用可能なフォントによっては、アルゴリズムに準拠して、ハングル文字またはボックスがランダムに表示されます。 |
|*FileName* |添付ファイルの名前。メッセージに表示されます。|
    
## <a name="examples-of-mapi-urls"></a>MAPI url の例

次に、MAPI url の例をいくつか示します。
  
- フォルダーの MAPI URL: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- メッセージの MAPI URL: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- 添付ファイルの MAPI URL: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>特殊文字

メッセージまたは添付ファイルに表示されている場合、特定の文字はエンコードされます。 次に、MAPI URL でエンコードされる文字を示します。
  
- % >% 25
    
- />% 2f 
    
- \ >% 5c 
    
- \*>% 2a 
    
- ? >% 3f 
    
## <a name="blob-associated-with-each-mapi-url"></a>各 MAPI URL に関連付けられている Blob

インデックスを作成するオブジェクトの mapi URL をプッシュするときに、ストアプロバイダーは、mapi プロトコルハンドラーの特定の情報を含むバイナリラージオブジェクト (BLOB) も作成します。 ストアプロバイダーは、この BLOB を各 mapi url に関連付け、mapi url をインデクサーにプッシュするときに送信します。 BLOB の形式は次のとおりです。 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

ストアプロバイダーは、表示されている順序でこれらの値を BLOB に書き込む必要があります。 次の表では、BLOB の各フィールドについて説明します。

|パーツ | 説明|
|:----|:-----------|  
|*dwversion* |これは、送信されるデータのバージョンです。 現在、この値は1です。|
|*dwFlags* |将来使用するために予約されています。 現在、この値は0である必要があります。|
|*cbprofilename* |プロファイル名のサイズ (バイト単位)。 この情報は、MAPI プロトコルハンドラーがアイテムのインデックス作成時に使用するプロファイルを知るのに役立ちます。|
|*wszProfileName* |プロファイル名を含む Null で終わる Unicode 文字列。|
|*cbprovideritemid* |プロバイダーアイテム ID のサイズ (バイト単位)。 ストアプロバイダーは、フォルダーのプロバイダアイテム ID のみを送信して、この情報を取得するために追加のフォルダーを開かないようにする必要があります。|
|*wszProviderItemID* |ストア内のアイテムを一意に識別するプロバイダアイテム ID を持つ、Null で終了する Unicode 文字列。|
    
## <a name="see-also"></a>関連項目

- [通知ベースのストアインデックス作成について](about-notification-based-store-indexing.md)
- [MAPI 定数](mapi-constants.md)

