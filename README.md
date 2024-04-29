<?php

$number = rand(0, 100);

echo $number . "\n";

$guess = -1;

$score = 0;

while ($guess != $number) {

    $guess = readline('Choisissez un nombre : ');
    if (!is_numeric($guess)) {
        echo "Merci de rentrer un nombre.\n";
    } else {
        $score = $score + 1;
        if ($guess > $number) {
            echo "C'est plus petit !\n";
        } else if ($guess < $number) {
            echo "C'est plus grand !\n";
        } else {
            echo "C'est gagné et votre score est de: $score ";
        }
    }
}
