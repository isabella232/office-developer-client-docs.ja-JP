---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 37651071bdc3ae99b4f374dcb7864a8f31dc1246
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614067"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既存のテーブルの先頭に列を追加または移動します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> [in]影響を受ける MAPI テーブルへのポインター。 
    
 _lpproptagColumnsNew_
  
> [in]テーブルの先頭に追加または移動するプロパティのプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。 
    
 _lpAllocateBuffer_
  
> [in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。 
    
 _lpfnFilterColumns_
  
> [in]呼び出し元によって提供されるコールバック関数へのポインター。 _lpfnFilterColumns パラメーター_ が NULL に設定されている場合、コールバックは実行できません。 
    
 _ptaga_
  
> [in]プロパティが先頭に追加または移動される前に、テーブルに既に存在するプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。 **HrAddColumnsEx** は、このポインターをパラメーターとして  _lpfnFilterColumns_ が指すコールバック関数に渡します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、指定された列が移動または追加されました。
    
## <a name="remarks"></a>注釈

_lpproptagColumnsNew_ パラメーターを使用して **HrAddColumnsEx** に渡されるプロパティは [、IMAPITable::QueryRows](imapitable-queryrows.md)メソッドへの後続の呼び出しで公開される最初のプロパティになります。 _lpproptagColumnsNew_ パラメーターで指定されていないテーブル内のすべてのプロパティは、追加および移動されたプロパティの後で公開されます。 
  
**QueryRows** が呼び出された場合、テーブル プロパティが未定義の場合は、プロパティの種類とプロパティPT_NULLプロパティ識別子を使用して返PROP_ID_NULL。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**HrAddColumnsEx** 関数を使用すると、呼び出し元はコールバック関数を提供して、テーブル内に既に存在していた列をフィルター処理できます 。たとえば、文字列をプロパティ型 PT_UNICODE から PT_STRING8 に変換します。 **HrAddColumnsEx** は、パラメーターとして以前に既存の列セットへのポインターをコールバック関数に渡します。 コールバック関数は、プロパティ タグ配列のデータを変更できますが、新しいタグを追加することはできません。 
  
 **HrAddColumnsEx** は、最初にコールバック関数が指定されている場合にコールバック関数を呼び出し、指定した列を追加または移動し、最後に [IMAPITable::SetColumns を呼び出します](imapitable-setcolumns.md)。 
  
_lpAllocateBuffer_ および _lpFreeBuffer_ 入力パラメーターは [、MAPIAllocateBuffer](mapiallocatebuffer.md)関数と [MAPIFreeBuffer](mapifreebuffer.md)関数をそれぞれ指します。 **HrAddColumnsEx** に渡されるポインターの正確な値は、呼び出し元がクライアント アプリケーションかサービス プロバイダーかによって異なります。 クライアントは、指定された名前を持つ MAPI 関数へのポインターを渡します。 サービス プロバイダーは、初期化呼び出しで受信したポインターを渡したり [、IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) メソッドを呼び出して取得します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

