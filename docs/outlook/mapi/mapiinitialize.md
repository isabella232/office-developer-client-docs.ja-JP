---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d22c24088960debcd18ccd818dad23656f6a01f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801513"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**適用対象**: Outlook 
  
MAPI サブシステムの参照カウントをインクリメントし、MAPI DLL のグローバル データを初期化します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>パラメーター

 _lpMapiInit_
  
> [in][MAPIINIT_0](mapiinit_0.md)構造体へのポインター。 _LpMapiInit_パラメーターを NULL に設定することができます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> MAPI サブシステムの初期化に成功しました。
    
## <a name="remarks"></a>注釈

MAPI のサブシステム、および[MAPIUninitialize](mapiuninitialize.md)関数をデクリメントの MAPI リファレンス カウントが**生じます**関数単位の内部参照カウントします。 したがって、1 つの関数への呼び出しの数は、他の呼び出しの数に等しくなければなりません。 **生じます**は、MAPI が以前に初期化されていない場合は S_OK を返します。 
  
クライアントまたはサービス プロバイダーは、他のすべての MAPI 呼び出しを行う前に**生じます**を呼び出す必要があります。 これを行うには、障害が発生すると、MAPI_E_NOT_INITIALIZED の値を取得するクライアントまたはサービス プロバイダーの呼び出しです。 
  
**生じます**マルチ スレッド アプリケーションから呼び出すと、次のように宣言されている[MAPIINIT_0](mapiinit_0.md)構造体に、 _lpMapiInit_パラメーターを設定します。 
  
 **MAPIINIT_0**MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
呼び出します。 
  
 **生じます**(&amp;MAPIINIT)。 
  
この構造体が宣言されると、MAPI は初期化の参照カウントがゼロに達するまで、通知ウィンドウを処理するために別のスレッドを作成します。 Windows サービスは、 **ulflags** 、 **MAPIINIT_0**構造体のメンバー MAPI_NT_SERVICE に_lpMapiInit_が指すを設定する必要があります。 
  
> [!NOTE]
> Win32 **DllMain**関数またはその他の機能を作成するか、スレッドを終了するのには**生じます**かから**MAPIUninitialize**を呼び出すことはできません。 詳細については、[スレッド セーフであるオブジェクトを使用する](using-thread-safe-objects.md)を参照してください。 
  
 **生じます**が、拡張エラー情報を返しません。 その他のほとんどの MAPI 呼び出しとは異なり、戻り値の意味は厳密には定義の初期化に失敗した特定の手順に対応します。 
  
1. パラメーターとフラグをチェックします。
    
    MAPI_E_INVALID_PARAMETER または MAPI_E_UNKNOWN_FLAGS です。 呼び出し元には、無効なパラメーターまたはフラグが渡されます。
    
2. MAPI によって必要なレジストリ キーを初期化し、オペレーティング システムの種類を確認します。 この手順は、クライアント プロセスは、windows サービスとして実行されているし、 **MAPIINIT_0**構造体の MAPI_NT サービス フラグを設定する場合にのみ発生します。 
    
    MAPI_E_TOO_COMPLEX。 呼び出し元のプロセスは、Windows サービスと、MAPI によって必要なレジストリ キーを初期化できませんでした。 
    
    詳細については、アプリケーション イベント ログで使用できる可能性があります。
    
3. Ole では、MAPI との互換性をチェックし、OLE を初期化します。
    
1. OLE の現在のバージョンと MAPI との互換性をチェックします。 
    
    MAPI_E_VERSION。 ワークステーションにインストールされている OLE のバージョンがこのバージョンの MAPI と互換性のあるされません。
    
2. OLE を初期化します。 
    
    この手順の場合にのみ、この関数は、記載されていないエラー コードを返すことができます。 何らかのエラーが表示_されない_ここでする必要がありますと見なされます、OLE 関数**CoInitialize**に由来します。
    
4. 初期化は、プロセスごとのグローバル変数です。
    
    MAPI_E_SESSION_LIMIT。 MAPI 設定コンテキストを現在のプロセスを特定します。 障害は、可能性がある場合に発生するプロセスの数は、特定の数を超えた場合、Win16 または任意のシステムで使用可能なメモリが不足します。
    
5. 初期化は、すべてのプロセスのグローバル変数を共有します。
    
    MAPI_E_NOT_ENOUGH_RESOURCES。 十分なシステム リソースは、操作を完了できませんでした。
    
6. 通知エンジンを初期化、MAPI_MULTITHREAD_NOTIFICATIONS フラグによって要求された場合、そのウィンドウとそのスレッドを作成します。 
    
    MAPI_E_INVALID_OBJECT。 システム リソースが使い果たされる場合があります。 
    
7. 読み込み、プロファイル プロバイダーを初期化します。 **生じます**が、プロファイル データが格納されているレジストリ キーにアクセスできることを確認します。 
    
    MAPI_E_NOT_INITIALIZED。 プロファイル プロバイダー エラーが発生しました。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> ||MFCMAPI では、いくつかのテーブルの処理を実行するのにバック グラウンド スレッドで MAPI を初期化するために**生じます**メソッドを使用します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

