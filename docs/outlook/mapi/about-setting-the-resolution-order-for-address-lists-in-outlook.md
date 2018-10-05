---
title: "Outlook �̃A�h���X�ꗗ�̉\U00011713x�̏�����ݒ肷����@"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391410"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>Outlook �̃A�h���X�ꗗ�̉𑜓x�̏�����ݒ肷����@

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルごとに複数のアドレス一覧をサポートしている Microsoft Office Outlook と電子メールの受信者がメッセージおよび会議出席依頼に出席者は解決されたアドレス一覧の順序を手動で指定できます。 たとえば、名が最初に Outlook アドレス帳、およびに対して、グローバル アドレス一覧に解決されるように、解決の順序を設定できます。 コンピューターでは、ユーザーがアドレス帳を開き、**ツール**と**オプション**をクリックし、この解決の順序を指定します。 ただし、企業環境でプログラムを使用して、名前が解決されるアドレス一覧の順序を設定するのには IT 管理者の方が効率的です。 このようなコードは、管理者が企業内に展開する起動自動化スクリプトの一部として使用できます。 
  
MAPI には、 **[IAddrBook](iaddrbookimapiprop.md)** インターフェイスは、名前解決に使用されるプロファイルに新しい検索パスを設定することで、 **[SetSearchPath](iaddrbook-getsearchpath.md)** メソッドがサポートされています。 **IAddrBook::SetSearchPath**メソッドを使用するには、関連のアドレスのコンテナーを保持する配列を使用して、目的の解像度の順序がそれらを解決する順序で書籍を指定する必要があります。 その配列内の各エントリには、対応するアドレス帳のエントリ ID を含める必要があります。 
  
�A�h���X�ꗗ�� [�J�X�^�������p�X��w�肷����@�̗����Ɏ����܂��B
  
- [アドレス一覧の解決順序をプログラムにより設定する](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [KB 292590: SetSearchPath �ƃA�h���X���̕��בւ�������ύX������@](https://support.microsoft.com/kb/292590)
    

