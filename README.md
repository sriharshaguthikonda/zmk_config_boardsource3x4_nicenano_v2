nice nano pinout. .
![image](https://github.com/sriharshaguthikonda/zmk_config_boardsource3x4_nicenano_v2/assets/16268244/ff145b9d-76cc-4aa6-b0db-a72ae394764a)


actual overlay


/* Copyright (c) 2020 The ZMK Contributors
 * SPDX-License-Identifier: MIT
 */
#include <dt-bindings/zmk/matrix_transform.h>
/ {
    chosen {
        zmk,kscan = &kscan0;
    };
    kscan0: kscan {
        compatible = "zmk,kscan-gpio-matrix";
        label = "KSCAN";
        diode-direction = "col2row";
 row-gpios
            = <&pro_micro 18 (GPIO_ACTIVE_HIGH | GPIO_PULL_DOWN)>
            , <&pro_micro 19 (GPIO_ACTIVE_HIGH | GPIO_PULL_DOWN)>
            , <&pro_micro 20 (GPIO_ACTIVE_HIGH | GPIO_PULL_DOWN)>             ;
 col-gpios
            = <&pro_micro 10 GPIO_ACTIVE_HIGH>
            , <&pro_micro 16 GPIO_ACTIVE_HIGH>
            , <&pro_micro 14 GPIO_ACTIVE_HIGH>
            , <&pro_micro 15 GPIO_ACTIVE_HIGH>            ;
    };
};
