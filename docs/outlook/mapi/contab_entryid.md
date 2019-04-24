---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a2a204f76b62c8c6bc6d8a4e793c936a0184dc65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335078"
---
# <a name="contabentryid"></a>CONTAB_ENTRYID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先フォルダーのエントリ ID を格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |msomapiutil  <br/> |
   
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

 **abflags**
  
> オブジェクトについての情報を提供するフラグのビットマスク。 詳細については、 [ENTRYID](entryid.md)構造の**abflags**フィールドの説明を参照してください。 
    
 **muid**
  
> ストアプロバイダーを識別する GUID。
    
 **ulversion**
  
> **CONTAB_ENTRYID**構造体のバージョン番号。 CONTAB_VERSION に設定する必要があります。 
    
 **ultype**
  
> 連絡先エントリ ID の種類を表す整数。 次のいずれかの値であることが必要です。
    
|**[名前]**|**[説明]**|
|:-----|:-----|
|CONTAB_USER  <br/> |メッセージングを処理するユーザー オブジェクトです。  <br/> |
|CONTAB_DISTLIST  <br/> |�z�z���X�g �I�u�W�F�N�g�ł��B  <br/> |
   
 **ulindex**
  
> 電子メールプロパティのサブセットに対するインデックス。
    
 **cbeid**
  
> 連絡先のアドレス帳で、このエントリに関連付けられている連絡先メッセージのエントリ id のサイズ。
    
 **abeid**
  
> 連絡先アドレス帳のこのエントリに関連付けられている連絡先メッセージのエントリ識別子。
    
## <a name="remarks"></a>解説

連絡先アドレス帳は、電子メールアドレスまたは fax 番号のいずれかの連絡先フォルダー内のすべての連絡先アイテムを含むアドレス帳です。 連絡先のアドレス帳の各エントリは、電子メールアドレスまたは fax 番号と関連付けられています。 連絡先アイテムは最大3つの電子メールアドレスと3つの fax 番号を持つことができるので、連絡先アイテムは対応する連絡先アドレス帳の最大6つのエントリで表すことができます。
  
連絡先アドレス帳の目的は、連絡先フォルダー内の連絡先に電子メールメッセージを送信するユーザーをサポートすることです。 microsoft outlook 2010 および microsoft outlook 2013 がサポートしている連絡先アドレス帳プロバイダーは contab32 です。
  
**CONTAB_ENTRYID**構造体は、基になる MAPI 連絡先メッセージ内に存在する情報のサブセットをサポートします。 特定の連絡先アドレス帳エントリに関連付けられている連絡先メッセージを識別します。 
  
**cbeid**および**abeid**フィールドは、 **ultype**フィールドの値が CONTAB_DISTLIST または CONTAB_USER に設定されている場合にのみ有効です。 **ultype**フィールドの値が CONTAB_ROOT、CONTAB_SUBROOT、または CONTAB_CONTAINER に設定されている場合は、代わりに[DIR_ENTRYID](dir_entryid.md)構造を使用する必要があります。 
  
## <a name="see-also"></a>関連項目



[DIR_ENTRYID](dir_entryid.md)


[MAPI の構造](mapi-structures.md)

