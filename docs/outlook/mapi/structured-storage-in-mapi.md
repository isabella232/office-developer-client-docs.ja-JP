---
title: MAPI のStorage構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: afc817e963a4855aaa5f13ee01b74a82e9ab225e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591032"
---
# <a name="structured-storage-in-mapi"></a>MAPI のStorage構造

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
構造化ストレージとは、COM で導入されたストレージの階層的な組織を指します。 構造化ストレージ環境では、記憶域は次の 2 種類または 3 種類のオブジェクトに編成されます。 
  
- Stream オブジェクト
    
- バイト オブジェクトのロック
    
- Storageオブジェクト
    
ストリームバイトとロック バイトは、データに直接アクセスする下位レベルのオブジェクトです。 Stream オブジェクトは **、データのバイトを** 読み取り、書き込み、配置、およびコピーするためのメソッドを定義する IStream インターフェイスを実装します。 Lock bytes オブジェクトは、バイト配列を使用してデータにアクセスするための別の COM インターフェイス **ILockBytes** を実装します。 バイト配列は、通常、基になる記憶域へのカスタマイズされたアクセスを提供するために使用されます。
  
Storageオブジェクトは、ストリーム オブジェクトまたはロック バイト オブジェクトの上に重なって表示されます。これらのオブジェクトには、1 つ以上のオブジェクトと他のストレージ オブジェクトを含めできます。 Storageは、入れ子になったオブジェクトを作成、アクセス、および管理するためのメソッドを定義する **IStorage** インターフェイスを実装します。 
  
**IStream、ILockBytes、** および **IStorage** は MAPI インターフェイスではなく COM インターフェイスなので、メソッドは MAPI 値ではなく COM エラー値を返します。  これらのインターフェイスでメソッドを呼び出すクライアントとサービス プロバイダーは、API 関数 **MapStorageSCode** を使用して、これらの値を MAPI エラー値に変換する必要があります。 詳細については [、「MapStorageSCode」を参照してください](mapstoragescode.md)。
  
クライアントとサービス プロバイダーは **、IMAPIProp** メソッド (通常は大きな文字列プロパティとバイナリ プロパティ) を維持するには大きすぎるプロパティを操作するために構造化ストレージを使用します。 クライアントまたはサービス プロバイダーがアクセスする一般的な方法の 1 つは [、IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドの呼び出しでインターフェイス識別子として **IStream** または **IStorage** を指定する方法です。 たとえば、クライアントは **OpenProperty** **を** プロパティ PR_ATTACH_DATA_BIN として呼び出し、IID_IStream をインターフェイス識別子として呼び出して、メッセージ内のバイナリ添付ファイルにアクセスします。 
  
クライアントとサービス プロバイダーは、独自のストリーム オブジェクトと記憶域オブジェクトを実装したり、API 関数を呼び出して、MAPI または COM によって提供される実装にアクセスできます。 提供される実装はほとんどの目的に役立つため、クライアントとサービス プロバイダーが独自の実装を作成する必要はほとんどありません。 
  
クライアントが MAPI オブジェクト **の OpenProperty** を呼び出して、ストレージ オブジェクトを介してプロパティの 1 つにアクセスすると、サービス プロバイダーは通常、直接モードでストレージ オブジェクトを開きます。 ただし、これは必須の動作ではなく一般的です。 クライアントは、サービス プロバイダーによって開かまたは作成されたストレージ オブジェクトはすべてトランザクション化され **、IStorage::Commit** への呼び出しが必要と想定する必要があります。 また、MAPI オブジェクトを保存する最後の Commit の後に **IMAPIProp::SaveChanges** を呼び出すまで、ストレージ オブジェクトへの変更は永続的に行ななわれたりしません。 詳細については [、「IMAPIProp::SaveChanges」を参照してください](imapiprop-savechanges.md)。
  
MAPI と COM には、ストレージ オブジェクトとストリーム オブジェクトを定義またはアクセスするためのいくつかの API 関数が備わっています。 一般的に使用される関数については、次の表で説明します。
  
**ストリーム オブジェクトとストリーム オブジェクトStorageアクセスする関数**

|**関数**|**説明**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |ストリームまたはロック バイト オブジェクトにアクセスするストレージ オブジェクトを作成します。  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |ストレージ オブジェクトにアクセスするメッセージ オブジェクトを作成します。  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |ファイルにアクセスするストリーム オブジェクトを作成します。  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |メッセージのリッチ テキストを保持するストリームの圧縮バージョンまたは非圧縮バージョンを含むストリーム オブジェクトを作成します。  <br/> |
   
 **特定のサブストルジ内のストリームの名前を取得するには**
  
1. **IEnumSTATSTG** インターフェイスを取得するには **、substorage の IStorage::EnumElements** メソッドを呼び出します。 
    
2. **IEnumSTATSTG::Next** を呼び出し、できる限り多くの **STATSTG** 構造を一度に呼び出します。 一度に 100 を求める場合は、通常 _、pceltFetched_ の内容が実際に取得された番号に設定された S_FALSE が返されます。 
    
3. アプリケーションでフラグ **が設定されている STATSTG** 構造STGTY_STREAM。 
    
4. _pwcsName パラメーターを解放_ します。 
    
 **既存のストリームまたはロック バイト オブジェクトにアクセスするストレージ オブジェクトを作成するには**
  
- クライアントは [HrIStorageFromStream を呼び出します](hristoragefromstream.md)。 
    
 **既存のストレージ オブジェクトにアクセスするメッセージ オブジェクトを作成するには**
  
- サービス プロバイダーとクライアントは [OpenIMsgOnIStg を呼び出します](openimsgonistg.md)。 作成されるメッセージ オブジェクトは **、IMessage::SubmitMessage** など、[すべての IMessage : IMAPIProp](imessageimapiprop.md)インターフェイス メソッドをサポートしていないという点で、メッセージ ストア プロバイダーによって通常作成されるメッセージ オブジェクトとは異なります。 **OpenIMsgOnIStg** へのオプションの入力パラメーターは [、MSGCALLRELEASE](msgcallrelease.md)プロトタイプに準拠するコールバック関数です。 この関数は、メッセージの参照カウントが 0 に達したときに、新しいメッセージ オブジェクトによって呼び出されます。 **MSGCALLRELEASE** 関数を実装すると、新しいメッセージが完全に削除される前に、最終的な処理を実行する場合に役立ちます。 
    
[OpenStreamOnFile](openstreamonfile.md) は、ファイルの読み取りと書き込みを行うストリームを作成するファイル添付ファイルの格納に一般的に使用されます。 **OpenProperty** プロパティ **PR_ATTACH_DATA_BIN** として指定すると、バイナリ添付ファイル データを格納するためのストリームが作成されます。 
  
 **リッチ テキスト形式でメッセージ テキストを含むストリームを圧縮または圧縮解除するには**
  
- クライアントは [WrapCompressedRTFStream を呼び出します](wrapcompressedrtfstream.md)。 **WrapCompressedRTFStream は** 、RTF ストリームをラップするストリームを作成します。 ラッパー ストリームは、すべての **IStream メソッドを実装する** 必要があります。次のメソッドは除外されます **。Seek**、SetSize、Revert、LockRegion、UnlockRegion、Stat、および **Clone** です。     **これは、WrapCompressedRTFStream** によって作成されたストリーム オブジェクトが **SetSize** または **Stat** をサポートしていないためです。サイズを拡張または取得する簡単な方法はありません。 最適な方法は、妥当なバッファー サイズを選択し、ループ内で読み取りまたは書き込みを行う方法です。
    
> [!NOTE]
> COM には、問題のある **EnumElements** メソッドから **IEnumSTATSTG** オブジェクトを返すバイト配列に基づくストレージ オブジェクトの実装があります。 特に **、QueryInterface** メソッドが正しく動作しません。 COM 実装を使用して独自のストレージ オブジェクトを実装するサービス プロバイダーは、基になる IEnumSTATSTG メソッドへの呼び出しを転送するが、独自の **AddRef** メソッド、Release メソッド **、QueryInterface** メソッド、**および Clone** メソッドを実装する **IEnumSTATSTG** オブジェクトのシン ラッパーを作成する必要があります。  
  

