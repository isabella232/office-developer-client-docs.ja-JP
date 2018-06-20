---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0e4e5d5910a7ff3551057760f065e79155d65e49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801202"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**適用されます**: Outlook 
  
呼び出し元のプロセスがメモリの指定された範囲に読み取りアクセス権を持っていることを確認します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapiwin.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダーです。  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> [in]Null で終わる ASCII 文字列へのポインター。
    
 _cchMax_
  
> [in]文字数、文字列の最大サイズです。 関数は、文字列の終端の null 文字までのすべての文字の読み取りアクセス権のチェック、またはこのパラメーターで指定された文字の数は、どちらかが小さい。 このパラメーターが 0 の場合は 0 を返します。
    
## <a name="return-value"></a>�߂�l

呼び出し元のプロセスが、文字列の終端の null 文字までのすべての文字への読み取りアクセスまたは_cchMax_で指定された文字数までの読み取りアクセス権を持つ場合は、0 を返します。
  
呼び出し元のプロセスが、文字列の終端の null 文字までのすべての文字への読み取りアクセスまたは_cchMax_で指定された文字数までの読み取りアクセス権があるないときは、0 以外を返します。
  
## <a name="remarks"></a>備考

**IsBadBoundedStringPtr**関数は、 **IsBadStringPtr**を使用すると同じです。
  
## <a name="see-also"></a>関連項目



[IsBadStringPtr](http://msdn.microsoft.com/en-us/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

