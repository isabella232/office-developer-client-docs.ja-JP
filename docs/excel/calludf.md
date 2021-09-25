---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f02b20c5a8355f68a937ad96cf4106c37f3a767a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614620"
---
# <a name="calludf"></a>CallUDF

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
高パフォーマンスのコンピューティング環境でユーザー定義関数を呼び出します。
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>パラメーター

_SessionId_
  
> �Ăяo����s���Z�b�V������ ID�B
    
_XLLName_
  
> ���[�U�[��`�֐����܂܂�� XLL �̖��O�B
    
_UDFName_
  
> ���[�U�[��`�֐��̖��O�B
    
_CallBackAddr_
  
> ���[�U�[��`�֐����I������Ƃ��ɃR�l�N�^���Ăяo���K�v������֐��B
    
_pxAsyncHandle_
  
> Excel �ƃR�l�N�^���A�ۗ����̃��[�U�[��`�֐��̌Ăяo����ǐՂ��邽�߂Ɏg�p����񓯊��n���h���B�R�l�N�^�ɂ���āA��قǁA�Ăяo�����I�������Ƃ� ( _CallBackAddr_ �����ɓn���ꂽ�֐��|�C���^�[��g�p���� Excel �ɃR�[���o�b�N����Ƃ�) �Ɏg�p����܂��B 
    
_ArgCount_
  
> ���[�U�[��`�֐��ɓn���������̐��B�ő�l�� 255 �ł��B
    
_Parameter1_
  
> ユーザー定義関数に渡す値。_ArgCount_ で指定されたパラメーターごとに、この引数を繰り返します。
    
## <a name="return-value"></a>戻り値

UDF 呼び出しが正常に開始された場合は **xlHpcRetSuccess** が返されます。_SessionId_ 引数が無効な場合は **xlHpcRetInvalidSessionId**、タイムアウトなどのその他のエラーが発生した場合は **xlHpcRetCallFailed** が返されます。呼び出しがエラー コード (**xlHpcRetSuccess** 以外のすべてのコード) を返すと、Excel は UDF 呼び出しが失敗したとみなし、_pxAsyncHandle_ を無効化します。この場合、Excel はコールバックが行われることを期待しません。
  
## <a name="remarks"></a>注釈

この関数は非同期で実行されます。
  
## <a name="see-also"></a>関連項目

- [Excel クラスター コネクタ関数](excel-cluster-connector-functions.md)

