#include <stdio.h>
#include <stdbool.h>
#include <time.h>
#include <stdlib.h>

typedef struct {
    int Air;
    double Grass;
    bool lightTime;
} Base;

bool light() {
    bool lightTime ;
    time_t now = time(NULL);
    struct tm *local_time = localtime(&now);
    int hour = local_time->tm_hour;
    int minute = local_time->tm_min;
    int second = local_time->tm_sec;

    if (hour >= 8 && hour < 20) {
        lightTime = true;
    } else {
        lightTime = false;
    }

    return lightTime;
}

int ProOxyg() {
    Base *base = (Base *)malloc(sizeof(Base));
    base->Air = 1;

    if (light()) {
        for (int i = 0; i <= 12; i++) {
            base->Air++;
        }
    } else {
        printf("Now is dark time\n");
    }

    return base->Air;
}

void Eat() {
    Base *base = (Base *)malloc(sizeof(Base));
    base->Grass = 1/0.0;
    int stomach = 0;

    if (light() && stomach == 0) {
        for (int i = 12; i >= 0; i--) {
            base->Grass--;
            stomach++;
        }
    } else {
        printf("Frog is not hungry\n");
        for (int i = 0; i <= 12; i++) {
            stomach--;
        }
        Eat();
    }
}

void Breath() {
    Base *base = (Base *)malloc(sizeof(Base));
    base->Air = 1;

    if (light()) {
        for (int i = 12; i >= 0; i--) {
            base->Air--;
        }
    } else {
        printf("Frog is sleeping now\n");
    }
}

int main() {
    bool test = light();
    if (test) {
        printf("Now we are living\n");
    }

    return 0;
}
