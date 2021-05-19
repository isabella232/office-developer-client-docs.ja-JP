---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a2a204f76b62c8c6bc6d8a4e793c936a0184dc65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424085"
---
# <a name="contab_entryid"></a>CONTAB_ENTRYID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先フォルダーのエントリ ID を格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |msomapiutil.h  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a>Members

 **abFlags**
  
> オブジェクトを説明する情報を提供するフラグのビットマスク。 詳細については [、ENTRYID](entryid.md)構造体の **abFlags** フィールドの説明を参照してください。 
    
 **muid**
  
> ストア プロバイダーを識別する GUID。
    
 **ulVersion**
  
> 構造のバージョン **番号CONTAB_ENTRYID** します。 この設定は、CONTAB_VERSION。 
    
 **ulType**
  
> 連絡先エントリ ID の種類を表す整数。 これは、次のいずれかの値である必要があります。
    
|**名前**|**説明**|
|:-----|:-----|
|CONTAB_USER  <br/> |メッセージングを処理するユーザー オブジェクトです。  <br/> |
|CONTAB_DISTLIST  <br/> |�z�z���X�g �I�u�W�F�N�g�ł��B  <br/> |
   
 **ulIndex**
  
> 電子メール プロパティのサブセットへのインデックス。
    
 **cbeid**
  
> 連絡先アドレス帳のこのエントリに関連付けられている連絡先メッセージのエントリ識別子のサイズ。
    
 **abeid**
  
> 連絡先アドレス帳のこのエントリに関連付けられている連絡先メッセージのエントリ識別子。
    
## <a name="remarks"></a>注釈

連絡先アドレス帳は、電子メール アドレスまたは FAX 番号を持つ連絡先フォルダー内のすべての連絡先アイテムを含むアドレス帳です。 連絡先アドレス帳の各エントリは、電子メール アドレスまたは FAX 番号に関連付けされます。 連絡先アイテムには最大 3 つの電子メール アドレスと 3 つの FAX 番号を含め、対応する連絡先アドレス帳内の最大 6 つのエントリで連絡先アイテムを表せません。
  
連絡先アドレス帳の目的は、連絡先フォルダー内の連絡先に電子メール メッセージをアドレス指定するユーザーをサポートします。 サポートとサポートをサポートMicrosoft Outlook 2010連絡先Microsoft Outlook 2013アドレス帳プロバイダーはcontab32.dll。
  
この **CONTAB_ENTRYID** は、基になる MAPI 連絡先メッセージに存在する情報のサブセットをサポートします。 特定の連絡先アドレス帳エントリが関連付けられている連絡先メッセージを識別します。 
  
**cbeid フィールドと** **abeid** フィールドは **、ulType** フィールドの値が設定されているフィールド値がCONTAB_DISTLISTまたはCONTAB_USER。 **ulType フィールドの** 値が CONTAB_ROOT、CONTAB_SUBROOT、CONTAB_CONTAINER に設定されている場合は、代DIR_ENTRYID構造を使用 [](dir_entryid.md)する必要があります。 
  
## <a name="see-also"></a>関連項目



[DIR_ENTRYID](dir_entryid.md)


[MAPI の構造](mapi-structures.md)

