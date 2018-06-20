---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 979415f1d792f92e593a7073cc84cfd6ba832b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803814"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**適用されます**: Outlook 
  
コピーのプロパティは、新しいターゲットに[SPropValue](spropvalue.md)構造体の配列によって定義されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _cprop_
  
> [in]コピーするプロパティの数です。 
    
 _rgprop_
  
> [in]コピーするプロパティを定義する[SPropValue](spropvalue.md)構造体の配列へのポインター。 _Rgprop_パラメーターを配列の先頭をポイントする必要はありませんが、 **SPropValue**構造体、配列内のいずれかの先頭を指している必要があります。 
    
 _pvDst_
  
> [in]この関数のプロパティをコピーする先のメモリ内の最初の位置へのポインター。 
    
 _pcb_
  
> [out]ポインターを_pvDst_パラメーターが指すメモリ ブロックのバイト単位のサイズを指します。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> プロパティが正常にコピーされました。
    
MAPI_E_INVALID_PARAMETER
  
> 不明なプロパティの種類が発生しました。
    
## <a name="remarks"></a>備考

新しい配列とそのデータは、1 つの割り当てで作成されたバッファー内に存在し、個別の[SPropValue](spropvalue.md)構造体のポインターを調整する[ScRelocProps](screlocprops.md)関数を使用することができます。 この調整をする前に、ポインターは有効です。 
  
 **ScCopyProps**は、コピーされたプロパティの配列を元のプロパティの順序を維持します。 
  
_Pcb_のパラメーターは省略可能です。それが NULL でない場合は、 _pvDst_パラメーターに格納されているバイト数に設定されています。 
  
## <a name="see-also"></a>関連項目



[ScDupPropset](scduppropset.md)

