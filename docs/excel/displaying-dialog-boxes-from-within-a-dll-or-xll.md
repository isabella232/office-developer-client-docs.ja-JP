---
title: 'title: "DLL �܂��� XLL �t�@�C���̒�����_�C�A���O �{�b�N�X��\������" ms.author: mroberts author: mroberts manager: soliver ms.date: 11/16/2014 ms.audience: Developer ms.topic: overview keywords:'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- 'xlls [excel 2007], displaying dialog boxes from,dialog boxes [Excel 2007], displaying from a DLL or XLL,DLLs [Excel 2007], displaying dialog boxes from ms.prod: office-online-server localization_priority: Normal ms.assetid: e77ac555-331d-41c8-a000-7b178959754d'
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'description: "�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio"'
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798782"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a>DLL �܂��� XLL �t�@�C���̒�����_�C�A���O �{�b�N�X��\������

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**] ダイアログ ボックス**では、Windows SDK の関数を使用して、Win32 ダイアログ ボックスを表示するのには Excel の完全 32 ビットのインスタンスとのメイン ウィンドウのハンドルを取得する必要があります最初。 詳細については、 [Excel のインスタンスをアクセスしメイン ウィンドウのハンドル](how-to-access-excel-instance-and-main-window-handles.md)を参照してください。 
  
ダイアログ ボックスのリソースがプロジェクトに含まれていると仮定した場合、行う必要があります処理ルーチンをダイアログ ボックスを閉じるときに Excel のメッセージを復元して、新しく表示されたダイアログ ボックスのメッセージ処理ルーチンを設定するのにはいくつか手順を実行します。 汎用的なプロジェクトでの使用例コマンド[fShowDialog](fshowdialog.md)は、これを正しく実行する Windows 関数の使用を示しています。 
  
C API を使用しても、ダイアログ ボックスを表示できます。この場合、Windows SDK 関数を使用する必要はありません。ただし、C API のダイアログ ボックスは、Windows、Visual Basic for Applications (VBA)、または Microsoft Foundation Classes (MFC) のものと比べて、機能が非常に制限されています。(たとえば、C API ダイアログ ボックスは常にモーダルです)。
  
## <a name="see-also"></a>�֘A����



[XLL ��쐬����](creating-xlls.md)
  
[DLL ��J������](developing-dlls.md)
  
[Excel のインスタンスをアクセスし、メイン ウィンドウのハンドル](how-to-access-excel-instance-and-main-window-handles.md)
  
[DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

