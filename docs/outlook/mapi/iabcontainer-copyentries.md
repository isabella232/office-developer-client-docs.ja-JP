---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346397"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つ以上のエントリ (通常はメッセージング ユーザーまたは配布リスト) をコピーします。
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpEntries_
  
> [in]コピーするエントリのエントリ識別子を含む [ENTRYLIST](entrylist.md) 構造体の配列へのポインター。 
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは、ulFlags パラメーターで AB_NO_DIALOGフラグが設定されている場合は _0 である必要_ があります。 
    
 _lpProgress_
  
> [in]進行状況インジケーター (NULL) を表示する進行状況オブジェクトへのポインター。 _lpProgress が_ NULL の場合は [、IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)メソッドを介して MAPI によって提供される進行状況オブジェクトを使用して進行状況インジケーターを表示する必要があります。 _lpProgress パラメーター_ は _、ulFlags_ で AB_NO_DIALOGフラグが設定されている場合は無視されます。
    
 _ulFlags_
  
> [in]コピー操作の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
AB_NO_DIALOG 
  
> 進行状況インジケーターの表示を抑制します。 このフラグが設定されていない場合は、進行状況インジケーターが表示されます。
    
CREATE_CHECK_DUP_LOOSE 
  
> 重複するエントリチェックの緩いレベルを実行する必要があります。 緩やかな重複エントリチェックの実装は、プロバイダー固有です。 たとえば、プロバイダーは、同じ表示名を持つ任意の 2 つのエントリとして緩やかな一致を定義できます。
    
CREATE_CHECK_DUP_STRICT 
  
> 厳密なレベルの重複エントリチェックを実行する必要があります。 厳密な重複エントリチェックの実装は、プロバイダー固有です。 たとえば、プロバイダーは、同じ表示名とメッセージング アドレスの両方を持つ任意の 2 つのエントリとして厳密な一致を定義できます。
    
CREATE_REPLACE 
  
> 2 つのエントリが重複すると判断された場合は、新しいエントリで既存のエントリを置き換える必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> コピー操作が成功しました。
    
MAPI_W_PARTIAL_COMPLETION 
  
> コピー操作は全体的に成功しましたが、1 つ以上のエントリをコピーする必要がありました。 この値が返されると、呼び出しは正常に処理されます。 この値をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IABContainer::CopyEntries メソッドは**、同じコンテナーまたは別のコンテナーからエントリをコピーします。 **CopyEntries の呼び出し** は、コピーするエントリごとに次の呼び出しを行うのと機能的に同等です。 
  
1. [新しいエントリを作成する IABContainer::CreateEntry](iabcontainer-createentry.md)メソッド。 
    
2. コピーするエントリからプロパティを読み取る [IMAPIProp::GetProps](imapiprop-getprops.md) メソッド。 
    
3. 新 [しいエントリにプロパティを書き込む IMAPIProp::SetProps](imapiprop-setprops.md) メソッド。 
    
4. 保存を実行する新 [しいエントリの IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッド。 
    
5. コンテナーの参照を解放する新しいエントリの [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) メソッド。 
    
## <a name="notes-to-implementers"></a>実装に関するメモ

**IABContainer::CopyEntries** メソッドをサポートするコンテナーはすべて、変更可能である必要があります。 コンテナーの AB_MODIFIABLE **フラグを** PR_CONTAINER_FLAGS ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティに設定して、変更可能であることを示します。 
  
すべてのフラグをサポートする必要があります。ただし、これらのフラグの解釈と使用は実装固有です。つまり、CREATE_CHECK_DUP_LOOSE フラグと CREATE_CHECK_DUP_STRICT フラグのセマンティクスが実装のコンテキストで何を意味するのかを判断できます。 エントリが重複するかどうかを判断できない場合、または判断できない場合は、常にエントリのコピーを許可します。 
  
CREATE_REPLACE フラグが設定されている場合は、CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT が設定されているかどうか、およびエントリが重複するかどうかに関係なく、常にエントリをコピーします。 
  
設定CREATE_REPLACE設定されていない場合は、CREATE_CHECK_DUP_STRICT重複を確認します。 エントリが重複と判断された場合は、そのエントリをコピーしない。 
  
サポートする必要CREATE_REPLACE。サポートされていないCREATE_REPLACE、安全に無視して、常にコピーを実行できます。 
  
重複しないエントリMAPI_W_PARTIAL_COMPLETIONコピーできない場合にのみ、警告メッセージを返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

コンテナーで重複CREATE_CHECK_DUP_LOOSEチェックCREATE_CHECK_DUP_STRICTする方法をプロバイダーに示すフラグを使用します。 重複するかどうかに関係なく、エントリを追加する必要がある場合は、これらのフラグを設定したり、CREATE_REPLACE フラグを設定したりしません。 CREATE_REPLACEは、エントリが重複している場合は気にしないかどうかを示します。常に元のエントリを置き換える必要があります。 
  
## <a name="see-also"></a>関連項目



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

