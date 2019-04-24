---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286933"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナー内のオブジェクトを開き、さらにアクセスするためのインターフェイスポインターを返します。
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番開くオブジェクトのエントリ識別子へのポインター。 _lな tryid_が NULL に設定されている場合、コンテナーの階層の最上位のコンテナーが開かれます。 
    
 _lpinterface_
  
> 順番オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 返されるオブジェクトの標準インターフェイスの識別子に NULL 結果が渡されます。 メッセージの場合、標準インターフェイスは[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md);フォルダーの場合は、 [imapifolder: IMAPIContainer](imapifolderimapicontainer.md)になります。 アドレス帳オブジェクトの標準インターフェイスは[idistlist: IMAPIContainer](idistlistimapicontainer.md)の配布リストと[idistlist: imapiprop](imailuserimapiprop.md)がメッセージングユーザーを対象としています。 
    
 _ulFlags_
  
> 順番オブジェクトを開く方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_BEST_ACCESS 
  
> ユーザーに対して許可される最大のネットワークアクセス許可と、クライアントアプリケーションの最大アクセス権を使用して、オブジェクトが開かれることを要求します。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、読み取り/書き込みアクセス許可を使用してオブジェクトを開く必要があります。クライアントが読み取り専用のアクセス権を持っている場合は、オブジェクトを読み取り専用アクセスで開く必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し元のクライアントがオブジェクトを完全に使用できるようになる前に、 **openentry**が正常に返されることを許可します。 オブジェクトが使用できない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用アクセスで開かれ、読み取り/書き込みアクセス許可が与えられているという前提でクライアントを使用することはできません。 
    
SHOW_SOFT_DELETES
  
> 現在、削除済みアイテムの保存期間の段階にあるとマークされているアイテムを表示します。
    
 _lpulobjtype_
  
> 読み上げ開かれているオブジェクトの種類へのポインター。
    
 _lppunk_
  
> 読み上げ開いているオブジェクトへのアクセスに使用するインターフェイス実装へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> オブジェクトが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> ユーザーがオブジェクトを開くための十分な権限を持っていないか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開こうとしています。
    
MAPI_E_NOT_FOUND 
  
> _lな tryid_で指定されたエントリ識別子は、オブジェクトを表していません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lな tryid_パラメーターのエントリ識別子が、コンテナーで認識される形式ではありません。 
    
## <a name="remarks"></a>解説

**IMAPIContainer:: openentry**メソッドは、コンテナー全体でオブジェクトを開き、さらにアクセスするために使用するインターフェイス実装へのポインターを返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lpinterface_パラメーターのインターフェイス識別子によって指定された型のインターフェイス実装を返す必要がないため、サービスプロバイダーは_lpulobjtype_パラメーターで示されている値を確認します。 必要に応じて、 _lppunk_で返されたポインターを、適切な型のポインターにキャストします。 
  
既定では、MAPI_MODIFY または MAPI_BEST_ACCESS フラグのどちらかを設定しない限り、サービスプロバイダーは読み取り専用アクセスでオブジェクトを開きます。 これらのフラグのいずれかが設定されている場合、サービスプロバイダーは変更可能なオブジェクトを取得しようとします。 ただし、開いているオブジェクトが読み取り/書き込みアクセス許可を持つ変更可能なオブジェクトを要求したため、このことを前提としていません。 その後の変更が失敗するかどうかを計画するか、またはオブジェクトの**PR_ACCESS_LEVEL**プロパティを取得して、 **openentry**によって付与されるアクセスレベルを判断します。
  
## <a name="see-also"></a>関連項目



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

