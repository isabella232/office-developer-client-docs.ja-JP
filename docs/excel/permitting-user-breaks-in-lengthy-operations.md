---
title: "���Ԃ̂����鑀��Ń��[�U�[�ɂ�钆�f����\x82���"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlabort function [excel 2007],concurrent tasks [Excel 2007],user breaks [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: b13f9b9a8c0e5621b25df13537632bdbe5dfc29e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798935"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a>���Ԃ̂����鑀��Ń��[�U�[�ɂ�钆�f�������

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Windows は、場所、機能やコマンドを実行するのには時間がかかることができます、プリエンプティブなマルチタス キングを使用している場合でもは、同時実行タスクのスケジュールを設定するために利用者からのオペレーティング システムにいくつかの時間を得ることをお勧めです。 Windows のネイティブの呼び出しを使用すると、これを行う、sleep 関数を使用しています。 C API を使用して、行うことができますそれを使用して、 [xlAbort 関数](xlabort.md)だけでなく、瞬時にプロセッサを生成、また、ユーザーが [キャンセル] キー、 **esc キー**を押したかどうかを参照してくださいを確認します。
  
���̌��ʁA **xlAbort** �֐��ɂ��A���[�U�[���v���Z�X��I�����A�K�v�ȃN���[���A�b�v����s���āAExcel �ɃR���g���[����Ԃ����ǂ�����R�[�h�Ŋm�F�ł��܂��B�܂��A���f��Ԃ������邱�Ƃ��ł��܂��B����ɂ��A���[�U�[���R�}���h��I�����邩�ǂ�����m�F����_�C�A���O �{�b�N�X��R�}���h�ŕ\���ł��܂��B�R�}���h��I�����Ȃ��ꍇ�́A����  **FALSE**  �� *xlAbort* �֐���Ăяo���āA���f�����ł��܂��B(����̈�����  *TRUE*  �ł��B����͏�Ԃ�m�F���邾���ŉ�����܂���B) 
  
���[�U�[��`�֐� (UDF) �� XLL �R�}���h���� **xlAbort** �֐���Ăяo�����Ƃ��ł��܂��BUDF �ł́A���[�U�[�ɂ�钆�f�����o����āA **xlAbort** �֐��� **TRUE** ��Ԃ��ꍇ�A�ʏ�A�֐��̌v�Z�����f����A�v�Z���������Ȃ��������Ƃ��������̒l (�G���[�� 0) ���Ԃ���܂��B���Ԃ̂�����֐��̑��̃C���X�^���X (�����悤�ɂ��̏�Ԃ�m�F����) ����f�����悤�ɁA���̒��f��Ԃ������Ȃ��ł��������BExcel �́A�Čv�Z�̏I�����ɂ��̏�Ԃ�ÖٓI�ɉ�����܂��B
  
Excel �̓R�}���h�̏I�����ɂ��̏�Ԃ�ÖٓI�ɉ�����܂����A�R�}���h�Œ��f��Ԃ����o���ꂽ�ꍇ�A�ʏ�͈��� **FALSE** �ɂ�� **xlAbort** �֐���Ăяo���ď�Ԃ������܂��B
  
## <a name="see-also"></a>�֘A����



[DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Excel �ł̃}���`�X���b�h�Čv�Z](multithreaded-recalculation-in-excel.md)
  
[Excel XLL �̊J��](developing-excel-xlls.md)
  
[Excel のインスタンスをアクセスし、メイン ウィンドウのハンドル](how-to-access-excel-instance-and-main-window-handles.md)

