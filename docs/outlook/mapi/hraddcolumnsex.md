---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 566a9d23c46ec717eb5eed711fff801b15d49fc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564235"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
追加または既存のテーブルの先頭に列を移動します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a>パラメーター

 _lptbl_
  
> [in]影響を MAPI テーブルへのポインター。 
    
 _lpproptagColumnsNew_
  
> [in]追加されたり、テーブルの先頭に移動するにはプロパティのプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
 _lpAllocateBuffer_
  
> [in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _lpfnFilterColumns_
  
> [in]呼び出し元によって提供されるコールバック関数へのポインター。 _LpfnFilterColumns_パラメーターは、NULL に設定されている場合、コールバックは行われません。 
    
 _ptaga_
  
> [in]プロパティ タグのプロパティを追加または先頭に移動する前にテーブルの既存の配列を格納する[SPropTagArray](sproptagarray.md)構造体へのポインター。 コールバック関数へのパラメーターとしては、このポインターが指す_lpfnFilterColumns_ **HrAddColumnsEx**のパス。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、指定された列の移動先または追加されました。
    
## <a name="remarks"></a>注釈

_LpproptagColumnsNew_パラメーターを使用して**HrAddColumnsEx**に渡されるプロパティは、 [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドへの後続の呼び出しで公開されている最初のプロパティになります。 追加、移動、すべてのプロパティの後は、 _lpproptagColumnsNew_パラメーターで指定されていないテーブルの以前の任意のプロパティが公開されています。 
  
**QueryRows**が呼び出されたときに、テーブルのプロパティは定義されていません、PT_NULL プロパティの型およびプロパティの識別子 PROP_ID_NULL に返されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**HrAddColumnsEx**関数は、既に PT_STRING8 プロパティの PT_UNICODE データ型から文字列に変換する例については、表にしていた列をフィルター処理するコールバック関数を提供する呼び出し元を使用できます。 **HrAddColumnsEx**は、コールバック関数へのパラメーターとして設定済みの既存の列へのポインターを渡します。 コールバック関数は、プロパティ タグ配列内のデータを変更できますが、新しいタグを追加することはできません。 
  
 **HrAddColumnsEx**は、1 つが提供され、追加または指定の列に移動し、最後に[IMAPITable::SetColumns](imapitable-setcolumns.md)を呼び出す場合に最初にコールバック関数を呼び出します。 
  
_LpAllocateBuffer_と_lpFreeBuffer_の入力パラメーターは、それぞれ、 [MAPIAllocateBuffer](mapiallocatebuffer.md)と[MAPIFreeBuffer](mapifreebuffer.md)関数をポイントします。 **HrAddColumnsEx**に渡されたポインターの正確な値は、呼び出し元が、クライアント アプリケーションまたはサービス プロバイダーによって異なります。 クライアントは、MAPI の関数を指定した名前にポインターを渡します。 ポインターの初期化の呼び出しで受信または[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)メソッドを呼び出すことによって取得されたことをサービス プロバイダーに渡します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

