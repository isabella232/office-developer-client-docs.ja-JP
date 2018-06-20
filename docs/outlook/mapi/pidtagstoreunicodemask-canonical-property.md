---
title: PidTagStoreUnicodeMask の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 010b17de08ee5836a26c56f300b36822df2e981e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803600"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a>PidTagStoreUnicodeMask の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
クライアント アプリケーションはメッセージ ストアの特性を決定するクエリを実行するためのフラグのビットマスクを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_STORE_UNICODE_MASK  <br/> |
|識別子:  <br/> |0x340F  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、メッセージを送信するクライアント アプリケーションにメッセージ ・ ストアの機能を公開します。 フラグは、クライアントまたは別のストア ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY** **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) をのみを送信するかどうかなど、意思決定を促進できます。 クライアントでは、このプロパティを設定する必要があることはありません。 しようとするには、 **MAPI_E_COMPUTED**をが返されます。 
  
次のフラグの 1 つ以上は、このプロパティを設定できます。 
  
STORE_ANSI_OK
  
> (131072、0x00020000)メッセージ ・ ストアは、米国規格協会 (ANSI) (8 ビット) 文字を含むプロパティをサポートしています。
    
STORE_ATTACH_OK 
  
> (32、0x00000020)メッセージ ・ ストアには、オブジェクトのリンクし埋め込み (OLE) または非 OLE 添付ファイルをメッセージがサポートされています。 
    
STORE_CATEGORIZE_OK 
  
> (1024、0x00000400)メッセージ ・ ストアでは、テーブルの分類されたビューをサポートします。 
    
STORE_CREATE_OK 
  
> (16、0x00000010)メッセージ ・ ストアには、新しいメッセージの作成がサポートされています。 
    
STORE_ENTRYID_UNIQUE 
  
> (1、0x00000001)エントリ、メッセージ ・ ストア内のオブジェクトの一意な識別子、つまり、ストアの有効期間中に使用されることです。 
    
STORE_HTML_OK 
  
> (65536、0x00010000)メッセージ ・ ストアは、 **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) のプロパティに格納されている HTML メッセージをサポートしています。 **STORE_HTML_OK**が MAPIDEFS のバージョンで定義されていないことに注意してください。含まれている Microsoft Exchange 2000 server 以前」をします。 場合は、開発環境は、MAPIDEFS を使用します。H ファイルではないには、 **STORE_HTML_OK**、"0x00010000"の値を代わりに使用します。 
    
STORE_ITEMPROC
  
> (2,097, 152、0x00200000)ラップされた PST ストア内をストアでは、新しいメッセージが到着すると、ストアは、ルールおよび迷惑メール フィルターとは別に、メッセージの処理を示します。 ストアの呼び出し[IMAPISupport::Notify](imapisupport-notify.md)、[通知](notification.md)の構造体をパラメーターとして渡され、リッスンしているクライアントに新しいメッセージの詳細を渡すには、設定**fnevNewMail** 。 その後、リッスンしているクライアントでは、通知を受信すると、メッセージのルールは処理されません。 
    
STORE_LOCALSTORE
  
> (524288、0x00080000)このフラグは予約されており、使用する必要があります。
    
STORE_MODIFY_OK 
  
> (8, 0x00000008)メッセージ ・ ストアには、既存のメッセージの変更がサポートしています。 
    
STORE_MV_PROPS_OK 
  
> (512、0x00000200)メッセージ ・ ストアが複数値を持つプロパティをサポートして、セーブセット全体で複数値を持つプロパティの値の順序の安定性を保証する操作、およびテーブル内の複数値を持つプロパティのインスタンス化をサポートしています。 
    
STORE_NOTIFY_OK 
  
> (256、0x00000100)メッセージ ・ ストアは、通知をサポートしています。 
    
STORE_OLE_OK 
  
> (64、0x00000040)メッセージ ・ ストアでは、OLE 添付ファイルをサポートしています。 OLE データは次のように、 **IStorage**インターフェイス経由でアクセスできる**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) は、その使用が可能です。 
    
STORE_PUBLIC_FOLDERS 
  
> (16384、0x00004000)このストア内のフォルダーは、パブリック (マルチ ユーザー)、非プライベート (可能性のある複数のインスタンスですが、マルチ ユーザーではなく)。 
    
STORE_PUSHER_OK
  
> (8,388, 608、0x00800000)MAPI プロトコル ハンドラーはストアをクロールしないと、ストアは、メッセージのインデックスを作成するのにはインデクサーに通知を使用して、変更をプッシュします。
    
STORE_READONLY 
  
> (2, 0x00000002)メッセージ ストアのすべてのインタ フェースでは、読み取り専用のアクセス レベルがあります。 
    
STORE_RESTRICTION_OK 
  
> (4096、0x00001000)メッセージ ・ ストアには、制限がサポートされています。 
    
STORE_RTF_OK 
  
> (2048、0x00000800)メッセージ ・ ストアは、リッチ テキスト形式 (RTF) メッセージは、通常は圧縮をサポートしていて、ストア自体が**PR_BODY**と**PR_RTF_COMPRESSED**の同期を維持します。 
    
STORE_SEARCH_OK 
  
> (4、0x00000004)メッセージ ・ ストアには、検索結果フォルダーがサポートしています。 
    
STORE_SORT_OK 
  
> (8192、0x00002000)メッセージ ・ ストアでは、テーブルのビューが並べ替えをサポートします。 
    
STORE_SUBMIT_OK 
  
> (128, 0x00000080)メッセージ ・ ストアは、メッセージ送信用のマークをサポートします。 
    
STORE_UNCOMPRESSED_RTF 
  
> (32768、0x00008000)メッセージ ・ ストアでは、未圧縮の形式でフォームの改訂可能なテキスト (RTF) メッセージの記憶域をサポートしています。 非圧縮の rtf 形式のストリームは、ストリームのヘッダーの値**dwMagicUncompressedRTF**で識別されます。 **DwMagicUncompressedRTF**値は、RTFLIB で定義されています。H ファイルです。 
    
STORE_UNICODE_OK
  
> (262144、0x00040000)メッセージ ・ ストアには、Unicode 文字を含むプロパティがサポートしています。
    
メッセージ ・ ストアが RTF に対応していない場合でも、rtf メッセージを保存常にできます。 STORE_RTF_OK ビットが特定のストアに設定されていない場合は、rtf 形式のバージョンを管理するクライアント自体関数を呼び出す必要[へ](rtfsync.md)テキストの内容を同期して**PR_BODY**と**PR_RTF_COMPRESSED**のバージョンを保持します。 Rtf 形式は、それが実際に圧縮するかどうかどうかに常に**PR_RTF_COMPRESSED**に格納されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

