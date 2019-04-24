---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348616"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージセッション内で使用するために、既存の OLE **IStorage**オブジェクトの上に新しい[IMessage](imessageimapiprop.md)オブジェクトを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a>パラメーター

_lpmsgsess_
  
> 順番新しい**IMessage**オブジェクトが作成されるメッセージセッションオブジェクトへのポインターを**** 指定します。 
    
_lpAllocateBuffer_
  
> 順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
_lpAllocateMore_
  
> 順番追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
_lpfreebuffer_
  
> 順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
_lpmalloc_
  
> 順番OLE **imalloc**インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。 **IMessage**インターフェイスは、 **IStorage**や**IStream**などのインターフェイスを使用するときに、この割り当て方法を使用する必要があります。 
    
_lpMapiSup_
  
> 順番(オプション) サービスプロバイダーが[imapisupport: IUnknown](imapisupportiunknown.md)インターフェイスのメソッドを呼び出すために使用できる MAPI サポートオブジェクトを指すポインターです。 
    
_lpstg_
  
> [入力]読み取り専用または読み取り/書き込みのアクセス許可を持つ、開いている OLE **IStorage**オブジェクトへのポインター。 **IMessage**は書き込み専用アクセスをサポートしていないため、 **OpenIMsgOnIStg**は書き込み専用モードで開かれたストレージオブジェクトを受け入れません。 
    
_lpfmsgcallrelease_
  
> 順番オプションのコールバック関数へのポインター。 [](msgcallrelease.md) MAPI は、 **IMessage**オブジェクト上の最後のリリースを呼び出した後に呼び出されます。 **** 
    
_ulcallerdata_
  
> 順番**IMessage**オブジェクトを使用して MAPI によって保存**** され、 **msgcallrelease**ベースのコールバック関数に渡される発信者データ。 このデータは、解放される**IMessage**オブジェクトと、それが作成された最初の**IStorage**オブジェクトに関するコンテキストを提供します。 
    
_ulFlags_
  
> 順番クライアントアプリケーションまたはサービスプロバイダーが**IMessage:: SaveChanges**メソッドを呼び出すときに、OLE **IStorage:: Commit**メソッドが呼び出されるかどうかを制御するために使用されるフラグのビットマスク。 次のフラグを設定できます。 
    
IMSG_NO_ISTG_COMMIT 
  
> OLE メソッド**IStorage:: Commit**は、クライアントまたはプロバイダーが[SaveChanges](imapiprop-savechanges.md)を呼び出したときには呼び出されません。 
    
MAPI_UNICODE
  
> Unicode .msg ファイルの作成を有効にします。 生成された[IMessage](imessageimapiprop.md)ファイルは、 [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)に STORE_UNICODE_OK を表示し、UNICODE プロパティをサポートします。 
    
  > [!NOTE]
  > MAPI_UNICODE フラグは、Outlook 2003 以降でのみ、この関数でサポートされています。 
  
_lppmsg_
  
> 読み上げ開いている**IMessage**オブジェクトへのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

property 属性は、プロパティオブジェクト (つまり、 [imapiprop: IUnknown](imapipropiunknown.md)インターフェイスを実装するオブジェクト) にのみアクセスできます。 ole 構造化ストレージオブジェクトで MAPI プロパティを使用できるようにするために、 **OpenIMsgOnIStg**は、ole **IStorage**オブジェクトの先頭に[IMessage: imapiprop](imessageimapiprop.md)オブジェクトをビルドします。 このようなオブジェクトのプロパティ属性は、 [SetAttribIMsgOnIStg](setattribimsgonistg.md)を使用して設定または変更したり、 [GetAttribIMsgOnIStg](getattribimsgonistg.md)で取得したりできます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**OpenIMsgOnIStg**を呼び出す前に、 [OpenIMsgSession](openimsgsession.md)を使用してメッセージセッションを開く必要があります。 有効な_lpmsgsess_パラメーターを指定すると、新しいメッセージがメッセージセッション内に作成され、セッションが閉じられるときに閉じられるようになります。 sures を実行してください。 _lpmsgsess_が NULL の場合、メッセージはメッセージセッションとは独立して作成されます。 メッセージを作成したクライアントアプリケーションまたはサービスプロバイダーが、そのメッセージをリリースしておらず、すべての添付ファイルと開いているテーブルを解放していない場合は、メモリがリークし、アプリケーションが終了する可能性があります。 
  
MAPI では、特に、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_が指す関数を使用して、オブジェクトインターフェイスを呼び出すときに使用するメモリをクライアントアプリケーションに割り当てます。[imapiprop:: GetProps](imapiprop-getprops.md) and [IMAPITable:: QueryRows](imapitable-queryrows.md)など。 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_の各ポインターは、有効な_lpMapiSup_パラメーターを指定して**OpenIMsgOnIStg**関数を呼び出した場合にオプションです。 
  
基になる ole オブジェクトを処理しているため、MAPI では ole メモリ割り当ても使用する必要があります。 ole 構造化ストレージオブジェクトと ole メモリ割り当ての詳細については、「 _ole プログラマーズリファレンス_」を参照してください。 
  
_lpMapiSup_に有効な値が指定されている場合、 **IMessage**は[imapisupport::D oprogress DIALOG](imapisupport-doprogressdialog.md)メソッドを呼び出して、imapisupport [:: CopyTo](imapiprop-copyto.md)の進行状況ユーザーインターフェイスを提供することにより、MAPI_DIALOG および ATTACH_DIALOG フラグをサポートします。[IMessage::D eleteattach](imessage-deleteattach.md)メソッド。 また、 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドは、 [imapisupport:: OpenAddressBook](imapisupport-openaddressbook.md)メソッドを呼び出して、生成されたアドレス帳オブジェクトに対して呼び出しを行うことによって、短期エントリ識別子を長期エントリ識別子に変換しようとします。 _lpMapiSup_に NULL が渡された場合、 **IMessage**は MAPI_DIALOG と ATTACH_DIALOG を無視し、短い用語エントリ識別子を変換せずに格納します。 
  
_lpstg_パラメーターが指す**IStorage**オブジェクトは、STGM_READ または STGM_READWRITE モードのどちらかで開く必要があります。 STGM_READWRITE モードが使用されている場合は、STGM_TRANSACTED モードも設定する必要があります。 
  
_lpfmsgcallrelease_パラメーターで指定されたコールバック関数はオプションです。指定する場合は、 [msgcallrelease](msgcallrelease.md)関数プロトタイプに基づいている必要があります。 **IMessage**インターフェイスは、 **IMessage**オブジェクトの参照カウントが、 **Release**メソッドへの**** 最後の呼び出しによって0に設定されたときに、それを呼び出します。 通常、コールバック関数は、基になる**IStorage**インターフェイスを解放するために使用されます。 **IMessage**は、コールバック後に_lpstg_パラメーターが指す**IStorage**オブジェクトへのアクセスを試みません。 
  
一部のクライアントまたはプロバイダーは、 [SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されたときに**IMessage**自体が書き込みを超える、 **IStorage**オブジェクトに追加のデータを書き込む場合があります。 クライアントまたはプロバイダーは、IMSG_NO_ISTG_COMMIT フラグを使用して、 **IMessage**が**SaveChanges**呼び出しの処理中に OLE **IStorage:: COMMIT**メソッドを呼び出さないようにすることができます。この場合、追加のデータが書き込まれたときに、クライアントまたはプロバイダー自体が**IStorage**オブジェクトをコミットする必要があります。 このため、 **IMessage**の実装では、文字列 "__" で始まる**IStorage**オブジェクト内に作成されるすべてのサブストレージの名前を指定する必要があります。つまり、アンダースコアは2つのアンダースコアで始まります。 クライアントまたはプロバイダーは、この名前空間のサブクラス名を保持することで、名前の競合を回避できます。 
  
MAPI では、添付ファイル、ストリーム、埋め込みメッセージなど、メッセージのサブオブジェクトに対して実行される複数の開いている操作の動作は定義されません。 現在、mapi では、既に開かれているサブオブジェクトをもう一度開くことができますが、mapi は、既存の開いているオブジェクトの参照カウントを増分し、そのオブジェクトを[IMessage:: openattach を呼び出したクライアントまたはプロバイダーに返すことで、open 操作を実行します。](imessage-openattach.md)または[imapiprop:: openproperty](imapiprop-openproperty.md)メソッド。 これは、サブファイルに対する最初の開いた操作に対して要求されたアクセスが、操作によって要求されたアクセス許可に関係なく、以降のすべてのオープン操作に対して提供されるアクセスであることを意味します。 
  
添付ファイルにメッセージを配置するための適切な手順は、IID_IMessage のインターフェイス識別子を使用して[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出すことです。 **openproperty**は現在、OLE **IStorage**インターフェイスで直接使用できるメッセージの添付ファイルの作成もサポートしています。つまり、IID_IStorage インターフェイス識別子を使用します。 **IStorage** access は、Microsoft Word 文書を OLE **IStream**インターフェイスに変換せずに添付ファイルに簡単に配置できるようにするためにサポートされています。 ただし、 **OpenIMsgOnIStg**に**IStorage**ポインターを添付ファイルデータに渡した後、オブジェクトが間違った順序で解放された場合、 **IMessage**は予測できない場合があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ファイル .cpp  <br/> |loadmsgtomessage  <br/> |mfcmapi は、 **OpenIMsgOnIStg**メソッドを使用して、の上に IMessage インターフェイスを開きます。MSG ファイルを使用して、ファイルが MAPI で操作されるようにします。  <br/> |
   
## <a name="see-also"></a>関連項目

- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

