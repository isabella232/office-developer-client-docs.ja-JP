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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 27a5978d85cf06a31f583b82cd39d0001852876b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801685"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**適用されます**: Outlook 
  
メッセージ セッション内で使用する、既存の OLE **IStorage**オブジェクトの上に新しい[IMessage](imessageimapiprop.md)オブジェクトを構築します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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

## <a name="parameters"></a>Parameters

_lpMsgSess_
  
> [in]- **IStorage**オブジェクトの新しい**IMessage**が作成される、メッセージ セッション オブジェクトへのポインター。 
    
_lpAllocateBuffer_
  
> [in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
_lpAllocateMore_
  
> [in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
_lpFreeBuffer_
  
> [in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
_lpMalloc_
  
> [in]OLE **IMalloc**インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。 **IMessage**インターフェイスは、 **IStorage**など**IStream**インターフェイスを使用する場合、この割り当てメソッドを使用する必要があります。 
    
_lpMapiSup_
  
> [in]サービス プロバイダーのメソッドの呼び出しに使用できる MAPI サポート オブジェクトへのポインターを省略可能な[IMAPISupport: IUnknown](imapisupportiunknown.md)インタ フェースです。 
    
_lpStg_
  
> [で [チェック アウト]OLE **IStorage**オブジェクトが開いている、読み取り専用または読み取り/書き込みのアクセス許可へのポインター。 **IMessage**が書き込み専用のアクセスをサポートしていないために、 **OpenIMsgOnIStg**は書き込み専用モードで開かれたストレージ オブジェクトを使用できません。 
    
_lpfMsgCallRelease_
  
> [in]-点灯 - **IStorage**オブジェクト**IMessage**の前回のリリースでは、次の呼び出しには、MAPI [MSGCALLRELEASE](msgcallrelease.md)プロトタイプに基づいてコールバック関数へのポインター ポインターです。 
    
_ulCallerData_
  
> [in]-点灯 - **IMessage** **IStorage**オブジェクトには MAPI によって保存され、 **MSGCALLRELEASE**に渡される呼び出し元のデータは、コールバック関数を基づいています。 データでは、リリースされている**IMessage**オブジェクトについてのコンテキストと上に構築された、 **IStorage**オブジェクトを提供します。 
    
_ulFlags_
  
> [in]クライアント アプリケーションまたはサービス プロバイダーは、 **IMessage::SaveChanges**メソッドを呼び出すと、OLE **IStorage::Commit**メソッドが呼び出されるかどうかは、コントロールに使用するフラグのビットマスクです。 次のフラグを設定することができます。 
    
IMSG_NO_ISTG_COMMIT 
  
> OLE メソッド**IStorage::Commit**は、クライアントまたはプロバイダーは、 [SaveChanges](imapiprop-savechanges.md)を呼び出すときに呼び出されるしません。 
    
MAPI_UNICODE
  
> Unicode の .msg ファイルを作成をできます。 [IMessage](imessageimapiprop.md)ファイルでは、その[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)に STORE_UNICODE_OK を示しています、Unicode プロパティをサポートしています。 
    
  > [!NOTE]
  > MAPI_UNICODE フラグは、Outlook 2003 またはそれ以降、この関数でのみサポートされます。 
  
_lppMsg_
  
> [out]開かれた**IMessage**オブジェクトへのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

プロパティの属性は、プロパティ オブジェクト、つまり、オブジェクトを実装することでのみアクセスできます、 [IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースです。 **OpenIMsgOnIStg**ビルドの MAPI プロパティを OLE 構造化ストレージ オブジェクトで使用できるようにするのには、 [IMessage: IMAPIProp](imessageimapiprop.md) OLE **IStorage**オブジェクト上にあるオブジェクトです。 このようなオブジェクトのプロパティの属性の設定または[SetAttribIMsgOnIStg](setattribimsgonistg.md)に変更し、 [GetAttribIMsgOnIStg](getattribimsgonistg.md)を取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**OpenIMsgOnIStg**が呼び出される前に[OpenIMsgSession](openimsgsession.md)でメッセージ セッションを開く必要があります。 Sures _lpMsgSess_の有効なパラメーターを指定するセッションが閉じられるときが閉じられているようにメッセージのセッション内で新しいメッセージを作成します。 _LpMsgSess_が NULL の場合は、メッセージの任意のセッションとは別にメッセージが作成されます。 場合、クライアント アプリケーションまたはメッセージを作成するサービス プロバイダーは、それと同様に、すべての添付ファイルを解放されず、テーブルを開き、メモリ リーク、アプリケーションが終了する可能性があります。 
  
MAPI が to で指された_lpAllocateBuffer_、 _lpAllocateMore_、および多くのメモリの割り当てと解放のための_lpFreeBuffer_具体的にはオブジェクトのインターフェイスを呼び出すときにクライアント アプリケーションで使用するメモリの割り当て関数を使用してください。[IMAPIProp::GetProps](imapiprop-getprops.md) 、 [IMAPITable::QueryRows](imapitable-queryrows.md)などです。 有効な_lpMapiSup_パラメーターを使用して、 **OpenIMsgOnIStg**関数が呼び出されたときに、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpFreeBuffer_のポインターはオプションです。 
  
基になる OLE オブジェクトを扱うにはため、MAPI が OLE メモリの割り当てを使用する必要があります。 OLE 構造化ストレージ オブジェクトと OLE のメモリの割り当ての詳細については、 _OLE プログラマ リファレンス_を参照してください。 
  
**IMessage**が[IMAPIProp::CopyTo](imapiprop-copyto.md)の進行状況のユーザー インターフェイスを提供する[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出すことによって、MAPI_DIALOG と ATTACH_DIALOG フラグをサポートする_lpMapiSup_の有効な値を入力する場合[IMessage::DeleteAttach](imessage-deleteattach.md)メソッドです。 また、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドは[IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md)メソッドを呼び出すと、結果のアドレス帳オブジェクトに呼び出しを行うことによって、長期のエントリ id を短期的なエントリの識別子を変換しようとします。 _LpMapiSup_に NULL を渡した場合、 **IMessage**は MAPI_DIALOG と ATTACH_DIALOG を無視し、変換せずに短期的なエントリの識別子を格納します。 
  
_LpStg_パラメーターが指す**IStorage**オブジェクトは、STGM_READ または STGM_READWRITE のいずれかのモードで開く必要があります。 STGM_READWRITE モードを使用する場合、STGM_TRANSACTED モードも設定しなければなりません。 
  
_LpfMsgCallRelease_パラメーターで指定されたコールバック関数は省略可能です。指定した場合に、 [MSGCALLRELEASE](msgcallrelease.md)関数のプロトタイプに基づいている必要があります。 -点灯 - **IMessage** **IStorage**オブジェクトの参照カウントは、 **Release**メソッドの最後の呼び出しによってゼロに設定されている場合、 **IMessage**インターフェイスを呼び出します。 コールバック関数は、基になっている**IStorage**インターフェイスを解放する通常使用されます。 **IMessage**は、コールバックを行った後、 _lpStg_パラメーターで示される**IStorage**オブジェクトにアクセスするのにはしません。 
  
いくつかのクライアントやプロバイダーは、追加のデータを書き込む可能性があります、 [SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されたときに書き込み自体**IMessage**をどのような**IStorage**オブジェクトにします。 クライアントまたはプロバイダーは、 **SaveChanges**の呼び出しの処理中に OLE **IStorage::Commit**メソッドを呼び出してから**IMessage**を防ぐために IMSG_NO_ISTG_COMMIT フラグを使用できます。ここでは、クライアントまたはプロバイダー コミットする必要が自体**IStorage**オブジェクト追加のデータが書き込まれるときです。 これに役立てるため、2 つのアンダー スコアでは、文字列「_ _」から始まる、 **IStorage**オブジェクトに作成し、すべての substorages に名前を付ける**IMessage**の実装を保証します。 クライアントまたはプロバイダーは、この名前空間からのサブストレージの名前を保持することで名前の衝突を回避できます。 
  
MAPI では、添付ファイル、ストリーム、または埋め込まれたメッセージなどのメッセージの下位で実行される複数の開く操作の動作は定義されていません。 MAPI が現在をもう一度開くオープンされているサブオブジェクトをことができますが、MAPI は、既存の開いているオブジェクトの参照カウントをインクリメントして、クライアント、IMessage::OpenAttach、[と呼ばれるプロバイダーに戻すことによってファイルを開く操作を実行](imessage-openattach.md)または[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドです。 これは、サブオブジェクトの最初の開く操作の要求されたアクセスの操作で要求されたアクセス権に関係なく、その後開く操作のアクセスを意味します。 
  
添付ファイルにメッセージを配置するための正しい手順では、IID_IMessage のインタ フェース識別子で[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出す。 **OpenProperty**現在の作成をサポート メッセージの添付ファイルが利用可能な OLE **IStorage**インターフェイス上で直接は、IID_IStorage インターフェイス識別子を使用します。 **IStorage**のアクセスをサポートして、簡単に OLE **IStream**インターフェイスとの間に変換せず、添付ファイルを Microsoft Word 文書を配置することを許可します。 ただし、 **OpenIMsgOnIStg**が添付ファイルのデータに、 **IStorage**ポインターを渡され、間違った順序でのオブジェクトの解放し、 **IMessage**が予測可能な動作しない可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI を開くには、IMessage インターフェイスの上に**OpenIMsgOnIStg**メソッドを使用して、します。MSG ファイルに MAPI でファイルを操作することがあります。  <br/> |
   
## <a name="see-also"></a>関連項目

- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

