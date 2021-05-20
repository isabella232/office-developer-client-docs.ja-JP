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
  
ファイルの内容にアクセスするために OLE **IStream** オブジェクトを割り当て、初期化します。 この関数は、パスとファイル拡張子を含むファイル名として ANSI 文字列を受け取ります。したがって、この関数の Unicode バージョン [である OpenStreamOnFileW](openstreamonfilew.md)の使用をお勧めします。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> [in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。 
    
 _ulFlags_
  
> [in]OLE IStream オブジェクトを介してアクセスするファイルの作成または開きを制御するために使用されるフラグ **のビット** マスク。 次のフラグを設定できます。 
    
SOF_UNIQUEFILENAME 
  
> IStream オブジェクト用に一時ファイル **を作成する必要** があります。 このフラグが設定されている場合は、STGM_CREATEおよびSTGM_READWRITEフラグも設定する必要があります。 
    
STGM_CREATE 
  
> ファイルは、既に存在している場合でも作成されます。 _lpszFileName_ パラメーターが設定されていない場合は、このフラグとSTGM_DELETEONRELEASE設定する必要があります。 このSTGM_CREATE設定されている場合は、STGM_READWRITEフラグも設定する必要があります。 
    
STGM_DELETEONRELEASE 
  
> **IStream** オブジェクトが解放されると、ファイルは削除されます。 _lpszFileName_ パラメーターが設定されていない場合は、このフラグとSTGM_CREATE設定する必要があります。 
    
STGM_READ 
  
> ファイルは、読み取り専用アクセスで作成または開く必要があります。 
    
STGM_READWRITE 
  
> ファイルを作成するか、読み取り/書き込み権限で開きます。 このフラグが設定されていない場合、STGM_CREATEフラグも設定できません。 
    
 _lpszFileName_
  
> [in] **OpenStreamOnFile** が **IStream** オブジェクトを初期化するファイルのファイル名 (パスと拡張子を含む)。 SOF_UNIQUEFILENAMEフラグが設定されている場合  _、lpszFileName_ には、一時ファイルを作成するディレクトリへのパスが含まれます。 _lpszFileName_ が NULL の場合 **、OpenStreamOnFile** はシステムから適切なパスを取得し、STGM_CREATE フラグと STGM_DELETEONRELEASE フラグの両方を設定する必要があります。 
    
 _lpszPrefix_
  
> [in] **OpenStreamOnFile** が IStream オブジェクトを初期化するファイル名 **のプレフィックス** 。 設定する場合、プレフィックスには 3 文字以内で指定する必要があります。 _lpszPrefix が_ NULL の場合は、"SOF" のプレフィックスが使用されます。 
    
 _lppStream_
  
> [out] **IStream** インターフェイスを公開するオブジェクトへのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_NO_ACCESS 
  
> ユーザーのアクセス許可が不足しているか、読み取り専用ファイルを変更できないため、ファイルにアクセスできません。 
    
MAPI_E_NOT_FOUND 
  
> 指定されたファイルが存在しません。
    
## <a name="remarks"></a>注釈

**OpenStreamOnFile** 関数には、2 つの重要な用途があります。このフラグの設定SOF_UNIQUEFILENAMEします。 このフラグを設定しない場合 **、OpenStreamOnFile** は既存のファイルで **IStream** オブジェクトを開きます。たとえば、その内容を **IStream::CopyTo** メソッドを使用して添付ファイルの **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティにコピーします。 この場合  _、lpszFileName_ パラメーターは、ファイルのパスとファイル名を指定します。 
  
このSOF_UNIQUEFILENAME **設定すると、OpenStreamOnFile** は IStream オブジェクトのデータを保持する一時ファイル **を作成** します。 この使用法では  _、lpszFileName_ パラメーターは、必要に応じて、ファイルを作成するディレクトリへのパスを指定し  _、lpszPrefix_ パラメーターはオプションでファイル名のプレフィックスを指定できます。 
  
呼び出し元のクライアント アプリケーションまたはサービス プロバイダーが **IStream** オブジェクトで終了したら、OLE **IStream::Release** メソッドを呼び出して解放する必要があります。 
  
MAPI は、ほとんどのメモリ割り当ておよび割り当て解除に  _lpAllocateBuffer_ と  _lpFreeBuffer_ が指す関数を使用します。特に [、IMAPIProp::GetProps](imapiprop-getprops.md) や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際に、クライアント アプリケーションで使用するメモリを割り当てる場合に使用します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ SOF_UNIQUEFILENAMEフラグを使用して、メッセージング システム固有の名前を持つ一時ファイルを作成します。 このフラグを設定すると  _、lpszFileName_ パラメーターは一時ファイルのパスを指定し  _、lpszPrefix_ パラメーターにはファイル名のプレフィックス文字が含まれています。 構築されたファイル名は <prefix> HHHH です。TMP。HHHH は 16 進数です。 _lpszFileName_ が NULL の場合、ファイルは Windows 関数 **GetTempPath** から返される一時ファイル ディレクトリ、または一時ファイル ディレクトリが指定されていない場合はカレント ディレクトリに作成されます。 
  
SOF_UNIQUEFILENAME フラグが設定されていない場合  _、lpszPrefix_ は無視され  _、lpszFileName_ には、開くまたは作成するファイルの完全修飾パスとファイル名を含む必要があります。 ファイルは  _、ulFlags_ で設定されている他のフラグに基づいて開かまたは作成されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|File.cpp  <br/> |WriteAttachStreamToFile  <br/> |MFCMAPI では **、OpenStreamOnFile** メソッドを使用してファイル上のストリームを開き、添付ファイルを書き出します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

