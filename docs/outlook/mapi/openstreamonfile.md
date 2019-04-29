---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439094"
---
# <a name="openstreamonfile"></a>OpenStreamOnFile

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
OLE **IStream**オブジェクトを割り当てて初期化し、ファイルの内容にアクセスします。 この関数は、パスとファイル拡張子を含むファイル名として ANSI 文字列を受け取ります。このため、 [openstreamonfilew](openstreamonfilew.md)の Unicode バージョンを使用することをお勧めします。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>パラメーター

 _lpAllocateBuffer_
  
> 順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpfreebuffer_
  
> 順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _ulFlags_
  
> 順番OLE **IStream**オブジェクトを通じてアクセスされるファイルの作成またはオープンを制御するために使用されるフラグのビットマスクです。 次のフラグを設定できます。 
    
SOF_UNIQUEFILENAME 
  
> **IStream**オブジェクトの一時ファイルが作成されます。 このフラグが設定されている場合は、STGM_CREATE と STGM_READWRITE のフラグも設定する必要があります。 
    
STGM_CREATE 
  
> ファイルは、既に存在している場合でも作成されます。 _lpszfilename_パラメーターが設定されていない場合は、このフラグと STGM_DELETEONRELEASE の両方を設定する必要があります。 STGM_CREATE が設定されている場合は、STGM_READWRITE フラグも設定する必要があります。 
    
STGM_DELETEONRELEASE 
  
> **IStream**オブジェクトが解放されるときに、ファイルを削除します。 _lpszfilename_パラメーターが設定されていない場合は、このフラグと STGM_CREATE の両方を設定する必要があります。 
    
STGM_READ 
  
> ファイルを作成するか、読み取り専用アクセスで開くかを指定します。 
    
STGM_READWRITE 
  
> ファイルは読み取り/書き込みアクセス許可で作成または開くことができます。 このフラグが設定されていない場合は、STGM_CREATE フラグを設定しないでください。 
    
 _lpszfilename_
  
> 順番**openstreamonfile**が**IStream**オブジェクトを初期化するファイルのパスと拡張子を含む filename。 SOF_UNIQUEFILENAME フラグが設定されている場合、 _lpszfilename_には、一時ファイルを作成するディレクトリへのパスが含まれます。 _lpszfilename_が NULL の場合、 **openstreamonfile**はシステムから適切なパスを取得し、STGM_CREATE と STGM_DELETEONRELEASE の両方のフラグを設定する必要があります。 
    
 _lpszprefix_
  
> 順番**openstreamonfile**が**IStream**オブジェクトを初期化するファイル名のプレフィックス。 設定されている場合、プレフィックスは3文字以下である必要があります。 _lpszprefix_が NULL の場合は、プレフィックス "SOF" が使用されます。 
    
 _lppstream_
  
> 読み上げ**IStream**インターフェイスを公開しているオブジェクトへのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_NO_ACCESS 
  
> ユーザーのアクセス許可が不足しているため、または読み取り専用ファイルを変更できないため、ファイルにアクセスできませんでした。 
    
MAPI_E_NOT_FOUND 
  
> 指定したファイルが存在しません。
    
## <a name="remarks"></a>注釈

**openstreamonfile**関数には、SOF_UNIQUEFILENAME フラグの設定によって区別される、2つの重要な用途があります。 このフラグが設定されていない場合、 **openstreamonfile**は、istream オブジェクトを既存のファイルに開きます。たとえば、 **** istream を使用して添付ファイルの**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティにコンテンツをコピーします。 **:: CopyTo**メソッド。 この場合、 _lpszfilename_パラメーターには、ファイルのパスとファイル名を指定します。 
  
SOF_UNIQUEFILENAME が設定されている場合、 **openstreamonfile**は**IStream**オブジェクトのデータを保持するための一時ファイルを作成します。 この使用法では、必要に応じて、ファイルを作成するディレクトリへのパスを_lpszfilename_パラメーターで指定できます。また、必要に応じて、 _lpszfilename_パラメーターでファイル名のプレフィックスを指定することもできます。 
  
呼び出し元クライアントアプリケーションまたはサービスプロバイダーが**IStream**オブジェクトで終了すると、OLE **istream:: Release**メソッドを呼び出して解放する必要があります。 
  
MAPI では、特に、 _lpAllocateBuffer_および_lpfreebuffer_で参照されている関数を使用して、imapiprop などのオブジェクトインターフェイスを呼び出すときに、クライアントアプリケーションが使用するメモリを割り当て[ます。GetProps](imapiprop-getprops.md)と[IMAPITable:: QueryRows](imapitable-queryrows.md)。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

SOF_UNIQUEFILENAME フラグは、メッセージングシステムに固有の名前を持つ一時ファイルを作成するために使用されます。 このフラグが設定されている場合、 _lpszfilename_パラメーターは一時ファイルのパスを指定し、 _lpszfilename_パラメーターにはファイル名の先頭文字が含まれます。 構築された<prefix>ファイル名は hhhhhhhh-hhhh-hhhh-hhhh-hhhhhhhhhhhh です。TMP、hhhhhhhh-hhhh-hhhh-hhhh-hhhhhhhhhhhh は16進数の数値です。 _lpszfilename_が NULL の場合は、Windows 関数**GetTempPath**から返される一時ファイルディレクトリ、または一時ファイルディレクトリが指定されていない場合は現在のディレクトリにファイルが作成されます。 
  
SOF_UNIQUEFILENAME フラグが設定されていない場合、 _lpszprefix_は無視され、 _lpszprefix_には開くまたは作成するファイルの完全修飾パスとファイル名が含まれている必要があります。 このファイルは、 _ulflags_に設定されている他のフラグに基づいて開かれるか作成されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ファイル .cpp  <br/> |writeattachstreamtofile  <br/> |mfcmapi は、 **openstreamonfile**メソッドを使用してファイルのストリームを開き、添付ファイルに書き出すことができるようにします。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

